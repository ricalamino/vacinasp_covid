<script>

	const idades_full = [
		{ id:1, idade: 59, ano: 2021, mes:6, dia:16},
		{ id:2, idade: 58, ano: 2021, mes:6, dia:16},
		{ id:3, idade: 57, ano: 2021, mes:6, dia:16},
		{ id:4, idade: 56, ano: 2021, mes:6, dia:16},
		{ id:5, idade: 55, ano: 2021, mes:6, dia:16},
		{ id:6, idade: 54, ano: 2021, mes:6, dia:16},
		{ id:7, idade: 53, ano: 2021, mes:6, dia:16},
		{ id:8, idade: 52, ano: 2021, mes:6, dia:16},
		{ id:9, idade: 51, ano: 2021, mes:6, dia:16},
		{ id:10, idade: 50, ano: 2021, mes:6, dia:16},
		{ id:11, idade: 49, ano: 2021, mes:6, dia:23},
		{ id:12, idade: 48, ano: 2021, mes:6, dia:23},
		{ id:13, idade: 47, ano: 2021, mes:6, dia:23},
		{ id:14, idade: 46, ano: 2021, mes:6, dia:23},
		{ id:15, idade: 45, ano: 2021, mes:6, dia:23},
		{ id:16, idade: 44, ano: 2021, mes:6, dia:23},
		{ id:17, idade: 43, ano: 2021, mes:6, dia:23},
		{ id:18, idade: 42, ano: 2021, mes:6, dia:30},
		{ id:19, idade: 41, ano: 2021, mes:6, dia:30},
		{ id:20, idade: 40, ano: 2021, mes:6, dia:30},
		{ id:21, idade: 39, ano: 2021, mes:7, dia:8},
		{ id:22, idade: 38, ano: 2021, mes:7, dia:8},
		{ id:23, idade: 37, ano: 2021, mes:7, dia:8},
		{ id:24, idade: 36, ano: 2021, mes:7, dia:15},
		{ id:25, idade: 35, ano: 2021, mes:7, dia:15},
		{ id:26, idade: 34, ano: 2021, mes:7, dia:19},
		{ id:27, idade: 33, ano: 2021, mes:7, dia:19},
		{ id:28, idade: 32, ano: 2021, mes:7, dia:19},
		{ id:29, idade: 31, ano: 2021, mes:7, dia:19},
		{ id:30, idade: 30, ano: 2021, mes:7, dia:19},
		{ id:31, idade: 29, ano: 2021, mes:7, dia:30},
		{ id:32, idade: 28, ano: 2021, mes:7, dia:30},
		{ id:33, idade: 27, ano: 2021, mes:8, dia:5},
		{ id:34, idade: 26, ano: 2021, mes:8, dia:5},
		{ id:35, idade: 25, ano: 2021, mes:8, dia:5},
		{ id:36, idade: 24, ano: 2021, mes:8, dia:10},
		{ id:37, idade: 23, ano: 2021, mes:8, dia:10},
		{ id:38, idade: 22, ano: 2021, mes:8, dia:10},
		{ id:39, idade: 21, ano: 2021, mes:8, dia:10},
		{ id:40, idade: 20, ano: 2021, mes:8, dia:10},
		{ id:41, idade: 19, ano: 2021, mes:8, dia:10},
		{ id:42, idade: 18, ano: 2021, mes:8, dia:10},
		{ id:43, idade: 17, ano: 2021, mes:8, dia:30},
		{ id:44, idade: 16, ano: 2021, mes:8, dia:30},
		{ id:45, idade: 15, ano: 2021, mes:8, dia:30},
		{ id:46, idade: 14, ano: 2021, mes:9, dia:6},
		{ id:47, idade: 13, ano: 2021, mes:9, dia:6},
		{ id:48, idade: 12, ano: 2021, mes:9, dia:6}
	];

	const cidade_idades_full = [
		{ id:1, idade: 59, ano: 2021, mes:6, dia:14},
		{ id:2, idade: 58, ano: 2021, mes:6, dia:14},
		{ id:3, idade: 57, ano: 2021, mes:6, dia:16},
		{ id:4, idade: 56, ano: 2021, mes:6, dia:16},
		{ id:5, idade: 55, ano: 2021, mes:6, dia:17},
		{ id:6, idade: 54, ano: 2021, mes:6, dia:17},
		{ id:7, idade: 53, ano: 2021, mes:6, dia:18},
		{ id:8, idade: 52, ano: 2021, mes:6, dia:18},
		{ id:9, idade: 51, ano: 2021, mes:6, dia:19},
		{ id:10, idade: 50, ano: 2021, mes:6, dia:19},
		{ id:11, idade: 49, ano: 2021, mes:6, dia:23},
		{ id:12, idade: 48, ano: 2021, mes:6, dia:24},
		{ id:13, idade: 47, ano: 2021, mes:6, dia:25},
		{ id:14, idade: 46, ano: 2021, mes:6, dia:28},
		{ id:15, idade: 45, ano: 2021, mes:6, dia:29},
		{ id:16, idade: 44, ano: 2021, mes:6, dia:29},
		{ id:17, idade: 43, ano: 2021, mes:6, dia:30},
		{ id:18, idade: 42, ano: 2021, mes:6, dia:30},
		{ id:19, idade: 41, ano: 2021, mes:7, dia:5},
		{ id:20, idade: 40, ano: 2021, mes:7, dia:7},
		{ id:21, idade: 39, ano: 2021, mes:7, dia:8},
		{ id:22, idade: 38, ano: 2021, mes:7, dia:9},
		{ id:23, idade: 37, ano: 2021, mes:7, dia:12},
		{ id:24, idade: 36, ano: 2021, mes:7, dia:15},
		{ id:25, idade: 35, ano: 2021, mes:7, dia:15},
		{ id:26, idade: 34, ano: 2021, mes:7, dia:19},
		{ id:27, idade: 33, ano: 2021, mes:7, dia:20},
		{ id:28, idade: 32, ano: 2021, mes:7, dia:21},
		{ id:29, idade: 31, ano: 2021, mes:7, dia:22},
		{ id:30, idade: 30, ano: 2021, mes:7, dia:23},
		{ id:31, idade: 29, ano: 2021, mes:7, dia:27},
		{ id:32, idade: 28, ano: 2021, mes:8, dia:2},
		{ id:33, idade: 27, ano: 2021, mes:8, dia:4},
		{ id:34, idade: 26, ano: 2021, mes:8, dia:5},
		{ id:35, idade: 25, ano: 2021, mes:8, dia:6},
		{ id:36, idade: 24, ano: 2021, mes:8, dia:10},
		{ id:37, idade: 23, ano: 2021, mes:8, dia:12},
		{ id:38, idade: 22, ano: 2021, mes:8, dia:13},
		{ id:39, idade: 21, ano: 2021, mes:8, dia:14},
		{ id:40, idade: 20, ano: 2021, mes:8, dia:14},
		{ id:41, idade: 19, ano: 2021, mes:8, dia:14},
		{ id:42, idade: 18, ano: 2021, mes:8, dia:14},
		{ id:43, idade: 17, ano: 2021, mes:8, dia:30},
		{ id:44, idade: 16, ano: 2021, mes:8, dia:30},
		{ id:45, idade: 15, ano: 2021, mes:8, dia:30},
		{ id:46, idade: 14, ano: 2021, mes:9, dia:6},
		{ id:47, idade: 13, ano: 2021, mes:9, dia:6},
		{ id:48, idade: 12, ano: 2021, mes:9, dia:6}
	];


	// Datas da última atualização de cada calendário
	const ultima_data_cidade = '11/08/2021';
	const ultima_data_estado = '29/07/2021';
	
	let selected = 1;
	
	const hoje = new Date();

	const idades = idades_full
									.filter(obj => hoje < new Date(obj.ano, obj.mes-1, obj.dia))
									.sort((a, b) => parseFloat(a.id) - parseFloat(b.id));

	selected = idades[0].id;

	let idade_selected = idades.find(obj => obj.id == selected);
	let	data_vacina = new Date(idade_selected.ano, idade_selected.mes-1, idade_selected.dia);  
	let	dias = Math.ceil((data_vacina-hoje)/(24*3600*1000));

	let meses_calculado = 0;
	let dias_calculado = 0;

	//municipio
	let cidade_selected = 1;
		
	const cidade_idades = cidade_idades_full
									.filter(obj => hoje < new Date(obj.ano, obj.mes-1, obj.dia))
									.sort((a, b) => parseFloat(a.id) - parseFloat(b.id));

	cidade_selected = cidade_idades[0].id;
					

	let cidade_idade_selected = cidade_idades.find(obj => obj.id == cidade_selected);
	let	cidade_data_vacina = new Date(cidade_idade_selected.ano, cidade_idade_selected.mes-1, cidade_idade_selected.dia);  
	let	cidade_dias = Math.ceil((cidade_data_vacina-hoje)/(24*3600*1000));

	let cidade_meses_calculado = 0;
	let cidade_dias_calculado = 0;

	function handleSubmit() {
		idade_selected = idades.find(obj => obj.id == selected);
		data_vacina = new Date(idade_selected.ano, idade_selected.mes-1, idade_selected.dia);  
		dias = Math.ceil((data_vacina-hoje)/(24*3600*1000));

		meses_calculado = parseInt(dias/30);
		dias_calculado = Math.ceil(dias%30);
	}

	function handleSubmitCidade() {
		cidade_idade_selected = cidade_idades.find(obj => obj.id == cidade_selected);
		cidade_data_vacina = new Date(cidade_idade_selected.ano, cidade_idade_selected.mes-1, cidade_idade_selected.dia);  
		cidade_dias = Math.ceil((cidade_data_vacina-hoje)/(24*3600*1000));

		cidade_meses_calculado = parseInt(cidade_dias/30);
		cidade_dias_calculado = Math.ceil(cidade_dias%30);
	}

</script>

<div class="container-sm shadow p-5 mb-5 mt-3 bg-body rounded">


	<ul class="nav nav-tabs" id="myTab" role="tablist">
		<li class="nav-item" role="presentation">
			<button class="nav-link active" id="home-tab" data-bs-toggle="tab" data-bs-target="#home" type="button" role="tab" aria-controls="home" aria-selected="true"><img src="./saopaulo.png" class="img-fluid" alt="" width="25px">&nbsp;&nbsp;Estado de São Paulo</button>
		</li>
		<li class="nav-item" role="presentation">
			<button class="nav-link" id="profile-tab" data-bs-toggle="tab" data-bs-target="#profile" type="button" role="tab" aria-controls="profile" aria-selected="false"><img src="./municipio.png" class="img-fluid" alt="" width="25px">&nbsp;&nbsp;Município de São Paulo</button>
		</li>
	</ul>
	<div class="tab-content" id="myTabContent">
		<div class="tab-pane fade show active" id="home" role="tabpanel" aria-labelledby="home-tab">
			
			<div class="row pt-3 pb-3">

				<div class="col-sm-3">
					<img src="./saopaulo.png" class="img-fluid" alt="">
				</div>
				<div class="col-sm-9">
					<h1>Vacinação no Estado de São Paulo</h1><span class="badge bg-danger">Novas datas! Atualizado em {ultima_data_estado}.</span>
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
			
			
			<div class="alert alert-success mt-3" role="alert">
				<p class="fs-3">Você será vacinado a partir do dia <strong>{idade_selected.dia< 10 ? '0'+idade_selected.dia: idade_selected.dia}/{idade_selected.mes < 10 ? '0'+idade_selected.mes: idade_selected.mes}/{idade_selected.ano}</strong>.</p>
				<p class="mb-0 fs-5">Falta{dias > 1 ? 'm' : ''} <strong>{dias} dia{dias > 1 ? 's' : ''}</strong> 
					{#if meses_calculado > 0} 
						( <strong>{meses_calculado} meses
						{#if dias_calculado > 0}
						e {dias_calculado} dias
						{/if}
						</strong>)
					{/if}
				para você tomar a primeira dose segundo o calendário oficial do Governo de São Paulo!</p>
			</div>

			<div class="alert alert-primary" role="alert">
				<strong>Atenção: Se você não encontrou sua idade, a vacinação da sua faixa etária já deve ter iniciado!</strong>
			</div>
			



		</div>
		<div class="tab-pane fade" id="profile" role="tabpanel" aria-labelledby="profile-tab">
		
			
			<div class="row pt-3 pb-3">

				<div class="col-sm-3">
					<img src="./municipio.png" class="img-fluid" alt="">
				</div>
				<div class="col-sm-9">
					<h1>Vacinação no Município de São Paulo</h1><span class="badge bg-danger">Novas datas! Atualizado em {ultima_data_cidade}.</span>
					<div class="row mt-3">
						<label for="colFormLabelLg" class="col-sm-6 col-form-label col-form-label-lg">Quantos anos você tem?</label>
						<div class="col-sm-6">
							<select bind:value={cidade_selected} on:change={handleSubmitCidade} on:blur={handleSubmitCidade} id="colFormLabelLg" class="form-select form-select-lg mb-1" aria-label=".form-select-lg example">
								<option selected id="0" value="0" disabled>Sua idade</option>
								{#each cidade_idades as cidade_idade}
									<option id={cidade_idade.id} value={cidade_idade.id}>
										{cidade_idade.idade}
									</option>
								{/each}
							</select>
						</div>
					</div>
				</div>
			</div>
			
			
			<div class="alert alert-warning mt-3" role="alert">
				<p class="fs-3">Você será vacinado a partir do dia <strong>{cidade_idade_selected.dia< 10 ? '0'+cidade_idade_selected.dia: cidade_idade_selected.dia}/{cidade_idade_selected.mes < 10 ? '0'+cidade_idade_selected.mes: cidade_idade_selected.mes}/{cidade_idade_selected.ano}</strong>.</p>
				<p class="mb-0 fs-5">Falta{cidade_dias > 1 ? 'm' : ''} <strong>{cidade_dias} dia{cidade_dias > 1 ? 's' : ''}</strong> 
					{#if cidade_meses_calculado > 0} 
						( <strong>{cidade_meses_calculado} meses
						{#if cidade_dias_calculado > 0}
						e {cidade_dias_calculado} dias
						{/if}
						</strong>)
					{/if}
				para você tomar a primeira dose segundo o calendário oficial do Município de São Paulo!</p>
			</div>

			<div class="alert alert-primary" role="alert">
				<strong>Atenção: Se você não encontrou sua idade, a vacinação da sua faixa etária já deve ter iniciado!</strong>
			</div>

			<!--<div class="alert alert-primary" role="alert">
				<strong>Atenção: Se você não encontrou sua idade, a vacinação da sua faixa etária já deve ter iniciado!</strong>
			</div>-->
		</div>
	</div>




	<hr />


	<p>Fonte: <a href="https://vacinaja.sp.gov.br/" target="_blank">vacinaja.sp.gov.br</a></p> 
	<p><a href="https://github.com/ricalamino/vacinasp_covid" ><img src="./github.png" alt="Github" width="32px" /></a></p>



</div>
