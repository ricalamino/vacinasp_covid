<script>

	const idades_full = [
		{ id:1, idade: 59, ano: 2021, mes:7, dia:1},
		{ id:2, idade: 58, ano: 2021, mes:7, dia:1},
		{ id:3, idade: 57, ano: 2021, mes:7, dia:1},
		{ id:4, idade: 56, ano: 2021, mes:7, dia:1},
		{ id:5, idade: 55, ano: 2021, mes:7, dia:1},
		{ id:6, idade: 54, ano: 2021, mes:8, dia:2},
		{ id:7, idade: 53, ano: 2021, mes:8, dia:2},
		{ id:8, idade: 52, ano: 2021, mes:8, dia:2},
		{ id:9, idade: 51, ano: 2021, mes:8, dia:2},
		{ id:10, idade: 50, ano: 2021, mes:8, dia:2},
		{ id:11, idade: 49, ano: 2021, mes:8, dia:17},
		{ id:12, idade: 48, ano: 2021, mes:8, dia:17},
		{ id:13, idade: 47, ano: 2021, mes:8, dia:17},
		{ id:14, idade: 46, ano: 2021, mes:8, dia:17},
		{ id:15, idade: 45, ano: 2021, mes:8, dia:17},
		{ id:16, idade: 44, ano: 2021, mes:9, dia:1},
		{ id:17, idade: 43, ano: 2021, mes:9, dia:1},
		{ id:18, idade: 42, ano: 2021, mes:9, dia:1},
		{ id:19, idade: 41, ano: 2021, mes:9, dia:1},
		{ id:20, idade: 40, ano: 2021, mes:9, dia:1},
		{ id:21, idade: 39, ano: 2021, mes:9, dia:11},
		{ id:22, idade: 38, ano: 2021, mes:9, dia:11},
		{ id:23, idade: 37, ano: 2021, mes:9, dia:11},
		{ id:24, idade: 36, ano: 2021, mes:9, dia:11},
		{ id:25, idade: 35, ano: 2021, mes:9, dia:11},
		{ id:26, idade: 34, ano: 2021, mes:9, dia:21},
		{ id:27, idade: 33, ano: 2021, mes:9, dia:21},
		{ id:28, idade: 32, ano: 2021, mes:9, dia:21},
		{ id:29, idade: 31, ano: 2021, mes:9, dia:21},
		{ id:30, idade: 30, ano: 2021, mes:9, dia:21},
		{ id:31, idade: 29, ano: 2021, mes:10, dia:1},
		{ id:32, idade: 28, ano: 2021, mes:10, dia:1},
		{ id:33, idade: 27, ano: 2021, mes:10, dia:1},
		{ id:34, idade: 26, ano: 2021, mes:10, dia:1},
		{ id:35, idade: 25, ano: 2021, mes:10, dia:1},
		{ id:36, idade: 24, ano: 2021, mes:10, dia:11},
		{ id:37, idade: 23, ano: 2021, mes:10, dia:11},
		{ id:38, idade: 22, ano: 2021, mes:10, dia:11},
		{ id:39, idade: 21, ano: 2021, mes:10, dia:11},
		{ id:40, idade: 20, ano: 2021, mes:10, dia:11},
		{ id:41, idade: 19, ano: 2021, mes:10, dia:11},
		{ id:42, idade: 18, ano: 2021, mes:10, dia:11}	
	];

	let selected;
	
	const hoje = new Date();

	const idades = idades_full
									.filter(obj => hoje <= new Date(obj.ano, obj.mes-1, obj.dia+1))
									.sort((a, b) => parseFloat(a.id) - parseFloat(b.id));

	let idade_selected ;
	let data_vacina ;  
	let dias ;

	let meses_calculado = 0;
	let dias_calculado = 0;

	function handleSubmit() {
		idade_selected = idades.find(obj => obj.id == selected);
		data_vacina = new Date(idade_selected.ano, idade_selected.mes-1, idade_selected.dia);  
		dias = parseInt((data_vacina-hoje)/(24*3600*1000));

		meses_calculado = parseInt(dias/30);
		dias_calculado = parseInt(dias%30);
	}

</script>

<div class="container-sm shadow p-5 mb-5 bg-body rounded">

	<div class="row pt-3 pb-3">

		<div class="col-sm-3">
			<img src="./saopaulo.png" class="img-fluid" alt="">
		</div>
		<div class="col-sm-9">
			<h1>Vacinação no Estado de São Paulo</h1>
			<div class="row mt-3">
				<label for="colFormLabelLg" class="col-sm-6 col-form-label col-form-label-lg">Quantos anos você tem?</label>
				<div class="col-sm-6">
					<select bind:value={selected} on:change={handleSubmit} on:blur={handleSubmit} id="colFormLabelLg" class="form-select form-select-lg mb-1" aria-label=".form-select-lg example">
						<option selected id="0" value="0" disabled>Sua idade</option>
						{#each idades as idade}
							<option id={idade.id} value={idade.id}>
								{idade.idade}
							</option>
						{/each}
					</select>
				</div>
			</div>
		</div>
	</div>
	
	{#if selected>0} 
		<div class="alert alert-success mt-3" role="alert">
			<p class="fs-3">Você será vacinado a partir do dia <strong>{idade_selected.dia< 10 ? '0'+idade_selected.dia: idade_selected.dia}/{idade_selected.mes < 10 ? '0'+idade_selected.mes: idade_selected.mes}/{idade_selected.ano}</strong>.</p>
			<p class="mb-0 fs-5">Faltam <strong>{dias} dias</strong> 
				{#if meses_calculado > 0} 
					( <strong>{meses_calculado} meses
					{#if dias_calculado > 0}
					e {dias_calculado} dias
					{/if}
					</strong>)
				{/if}
			para você tomar a primeira dose segundo o calendário oficial do Governo de São Paulo!</p>
		</div>
	{/if}

	<hr />

	<div class="flourish-embed" data-src="story/720615"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

	<hr />

	<p>Fonte: <a href="https://vacinaja.sp.gov.br/" target="_blank">https://vacinaja.sp.gov.br/</a></p> 

	<hr />

</div>
