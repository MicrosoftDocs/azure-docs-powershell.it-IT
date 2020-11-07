---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 219e5b18a04332d2ee840fb41b92aa9d282a1792
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865265"
---
# <span data-ttu-id="048c3-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="048c3-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="048c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="048c3-102">SYNOPSIS</span></span>
<span data-ttu-id="048c3-103">Crea una data factory.</span><span class="sxs-lookup"><span data-stu-id="048c3-103">Creates a data factory.</span></span>

## <span data-ttu-id="048c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="048c3-104">SYNTAX</span></span>

### <span data-ttu-id="048c3-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="048c3-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="048c3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="048c3-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="048c3-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="048c3-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="048c3-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="048c3-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="048c3-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="048c3-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="048c3-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="048c3-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="048c3-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="048c3-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="048c3-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="048c3-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="048c3-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="048c3-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="048c3-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="048c3-114">DESCRIPTION</span></span>
<span data-ttu-id="048c3-115">Il cmdlet **set-AzDataFactoryV2** crea una factory di dati con il nome e il percorso del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="048c3-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="048c3-116">Eseguire queste operazioni nell'ordine seguente:--creare una factory di dati.</span><span class="sxs-lookup"><span data-stu-id="048c3-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="048c3-117">--Creare servizi collegati.</span><span class="sxs-lookup"><span data-stu-id="048c3-117">-- Create linked services.</span></span>
<span data-ttu-id="048c3-118">--Creare DataSet.</span><span class="sxs-lookup"><span data-stu-id="048c3-118">-- Create datasets.</span></span>
<span data-ttu-id="048c3-119">--Crea una pipeline.</span><span class="sxs-lookup"><span data-stu-id="048c3-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="048c3-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="048c3-120">EXAMPLES</span></span>

### <span data-ttu-id="048c3-121">Esempio 1: creare una data factory</span><span class="sxs-lookup"><span data-stu-id="048c3-121">Example 1: Create a data factory</span></span>
```
PS C:\> Set-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration :
```

### <span data-ttu-id="048c3-122">Esempio 2: creare una factory di dati con i dettagli di configurazione di repo usando un oggetto factory esistente.</span><span class="sxs-lookup"><span data-stu-id="048c3-122">Example 2: Create a data factory with repo configuration details using an existing factory object.</span></span>
```
PS C:\> Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" | Set-AzDataFactoryV2 -AccountName msdata -RepositoryName ADFRepo -CollaborationBranch master -RootFolder / -ProjectName "Azure Data Factory"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration : Microsoft.Azure.Management.DataFactory.Models.FactoryVSTSConfiguration
```

<span data-ttu-id="048c3-123">Questo comando crea una factory di dati denominata WikiADF nel gruppo di risorse denominato ADF nella posizione Eastus con la configurazione del controllo del codice sorgente di Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="048c3-123">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with Azure DevOps source control configuration.</span></span>

### <span data-ttu-id="048c3-124">Esempio 3: creare un data factory con i dettagli di configurazione di GitHub repo usando un nuovo oggetto Factory.</span><span class="sxs-lookup"><span data-stu-id="048c3-124">Example 3: Create a data factory with GitHub repo configuration details using a new factory object.</span></span>
```
PS C:\> New-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location 'EastUS' -HostName 'https://github.com' -AccountName msdata -RepositoryName ADFRepo -CollaborationBranch master -RootFolder /

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration : Microsoft.Azure.Management.DataFactory.Models.FactoryGitHubConfiguration
```

<span data-ttu-id="048c3-125">Questo comando crea una factory di dati denominata WikiADF nel gruppo di risorse denominato ADF nella posizione Eastus con la configurazione del controllo del codice sorgente di GitHub.</span><span class="sxs-lookup"><span data-stu-id="048c3-125">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with GitHub source control configuration..</span></span>

## <span data-ttu-id="048c3-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="048c3-126">PARAMETERS</span></span>

### <span data-ttu-id="048c3-127">-AccountName</span><span class="sxs-lookup"><span data-stu-id="048c3-127">-AccountName</span></span>
<span data-ttu-id="048c3-128">Nome dell'account per la configurazione di repo.</span><span class="sxs-lookup"><span data-stu-id="048c3-128">The account name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048c3-129">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="048c3-129">-CollaborationBranch</span></span>
<span data-ttu-id="048c3-130">Ramo collaborazione per la configurazione dei repo.</span><span class="sxs-lookup"><span data-stu-id="048c3-130">The collaboration branch for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048c3-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="048c3-131">-DefaultProfile</span></span>
<span data-ttu-id="048c3-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="048c3-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048c3-133">-Force</span><span class="sxs-lookup"><span data-stu-id="048c3-133">-Force</span></span>
<span data-ttu-id="048c3-134">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="048c3-134">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048c3-135">-HostName</span><span class="sxs-lookup"><span data-stu-id="048c3-135">-HostName</span></span>
<span data-ttu-id="048c3-136">Nome host per la configurazione repo di GitHub.</span><span class="sxs-lookup"><span data-stu-id="048c3-136">The host name for GitHub repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048c3-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="048c3-137">-InputObject</span></span>
<span data-ttu-id="048c3-138">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="048c3-138">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="048c3-139">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="048c3-139">-LastCommitId</span></span>
<span data-ttu-id="048c3-140">L'ultimo ID commit per la configurazione di repo.</span><span class="sxs-lookup"><span data-stu-id="048c3-140">The last commit id for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048c3-141">-Posizione</span><span class="sxs-lookup"><span data-stu-id="048c3-141">-Location</span></span>
<span data-ttu-id="048c3-142">La factory di dati viene creata nell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="048c3-142">The data factory is created in this region.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="048c3-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="048c3-143">-Name</span></span>
<span data-ttu-id="048c3-144">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="048c3-144">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="048c3-145">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="048c3-145">-ProjectName</span></span>
<span data-ttu-id="048c3-146">Il nome di progetto Azure DevOps per la configurazione di repo.</span><span class="sxs-lookup"><span data-stu-id="048c3-146">The project name Azure DevOps for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048c3-147">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="048c3-147">-RepositoryName</span></span>
<span data-ttu-id="048c3-148">Nome del repository per la configurazione di repo.</span><span class="sxs-lookup"><span data-stu-id="048c3-148">The repository name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048c3-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="048c3-149">-ResourceGroupName</span></span>
<span data-ttu-id="048c3-150">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="048c3-150">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="048c3-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="048c3-151">-ResourceId</span></span>
<span data-ttu-id="048c3-152">ID risorsa Azure di V2 Data Factory.</span><span class="sxs-lookup"><span data-stu-id="048c3-152">The Azure resource ID of V2 data factory.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig
Aliases: Id, DataFactoryId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="048c3-153">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="048c3-153">-RootFolder</span></span>
<span data-ttu-id="048c3-154">Cartella radice per la configurazione di repo.</span><span class="sxs-lookup"><span data-stu-id="048c3-154">The root folder for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048c3-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="048c3-155">-Tag</span></span>
<span data-ttu-id="048c3-156">Tag della data factory.</span><span class="sxs-lookup"><span data-stu-id="048c3-156">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFactoryName, ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="048c3-157">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="048c3-157">-TenantId</span></span>
<span data-ttu-id="048c3-158">ID tenant per la configurazione di repository di Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="048c3-158">The tenant id for Azure DevOps repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048c3-159">-Confermare</span><span class="sxs-lookup"><span data-stu-id="048c3-159">-Confirm</span></span>
<span data-ttu-id="048c3-160">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="048c3-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048c3-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="048c3-161">-WhatIf</span></span>
<span data-ttu-id="048c3-162">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="048c3-162">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048c3-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="048c3-163">CommonParameters</span></span>
<span data-ttu-id="048c3-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="048c3-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="048c3-165">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="048c3-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="048c3-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="048c3-166">INPUTS</span></span>

### <span data-ttu-id="048c3-167">System. String</span><span class="sxs-lookup"><span data-stu-id="048c3-167">System.String</span></span>

### <span data-ttu-id="048c3-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="048c3-168">System.Collections.Hashtable</span></span>

## <span data-ttu-id="048c3-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="048c3-169">OUTPUTS</span></span>

### <span data-ttu-id="048c3-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="048c3-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="048c3-171">Note</span><span class="sxs-lookup"><span data-stu-id="048c3-171">NOTES</span></span>
<span data-ttu-id="048c3-172">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="048c3-172">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="048c3-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="048c3-173">RELATED LINKS</span></span>

[<span data-ttu-id="048c3-174">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="048c3-174">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="048c3-175">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="048c3-175">Remove-AzDataFactoryV2</span></span>]()
