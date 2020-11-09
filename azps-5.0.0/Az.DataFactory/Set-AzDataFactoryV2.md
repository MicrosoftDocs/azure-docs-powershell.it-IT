---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 5020ddeccc755ef52bf7410d61eb57b637d261bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298261"
---
# <span data-ttu-id="3cfc9-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3cfc9-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="3cfc9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3cfc9-102">SYNOPSIS</span></span>
<span data-ttu-id="3cfc9-103">Crea una data factory.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-103">Creates a data factory.</span></span>

## <span data-ttu-id="3cfc9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3cfc9-104">SYNTAX</span></span>

### <span data-ttu-id="3cfc9-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3cfc9-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cfc9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3cfc9-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cfc9-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="3cfc9-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cfc9-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="3cfc9-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cfc9-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="3cfc9-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cfc9-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="3cfc9-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cfc9-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3cfc9-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cfc9-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="3cfc9-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cfc9-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="3cfc9-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cfc9-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3cfc9-114">DESCRIPTION</span></span>
<span data-ttu-id="3cfc9-115">Il cmdlet **set-AzDataFactoryV2** crea una factory di dati con il nome e il percorso del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="3cfc9-116">Eseguire queste operazioni nell'ordine seguente:--creare una factory di dati.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="3cfc9-117">--Creare servizi collegati.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-117">-- Create linked services.</span></span>
<span data-ttu-id="3cfc9-118">--Creare DataSet.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-118">-- Create datasets.</span></span>
<span data-ttu-id="3cfc9-119">--Crea una pipeline.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="3cfc9-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3cfc9-120">EXAMPLES</span></span>

### <span data-ttu-id="3cfc9-121">Esempio 1: creare una data factory</span><span class="sxs-lookup"><span data-stu-id="3cfc9-121">Example 1: Create a data factory</span></span>
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

### <span data-ttu-id="3cfc9-122">Esempio 2: creare una factory di dati con i dettagli di configurazione di repo usando un oggetto factory esistente.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-122">Example 2: Create a data factory with repo configuration details using an existing factory object.</span></span>
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

<span data-ttu-id="3cfc9-123">Questo comando crea una factory di dati denominata WikiADF nel gruppo di risorse denominato ADF nella posizione Eastus con la configurazione del controllo del codice sorgente di Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-123">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with Azure DevOps source control configuration.</span></span>

### <span data-ttu-id="3cfc9-124">Esempio 3: creare un data factory con i dettagli di configurazione di GitHub repo usando un nuovo oggetto Factory.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-124">Example 3: Create a data factory with GitHub repo configuration details using a new factory object.</span></span>
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

<span data-ttu-id="3cfc9-125">Questo comando crea una factory di dati denominata WikiADF nel gruppo di risorse denominato ADF nella posizione Eastus con la configurazione del controllo del codice sorgente di GitHub.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-125">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with GitHub source control configuration..</span></span>

## <span data-ttu-id="3cfc9-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3cfc9-126">PARAMETERS</span></span>

### <span data-ttu-id="3cfc9-127">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3cfc9-127">-AccountName</span></span>
<span data-ttu-id="3cfc9-128">Nome dell'account per la configurazione di repo.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-128">The account name for repo configuration.</span></span>

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

### <span data-ttu-id="3cfc9-129">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="3cfc9-129">-CollaborationBranch</span></span>
<span data-ttu-id="3cfc9-130">Ramo collaborazione per la configurazione dei repo.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-130">The collaboration branch for repo configuration.</span></span>

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

### <span data-ttu-id="3cfc9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cfc9-131">-DefaultProfile</span></span>
<span data-ttu-id="3cfc9-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cfc9-133">-Force</span><span class="sxs-lookup"><span data-stu-id="3cfc9-133">-Force</span></span>
<span data-ttu-id="3cfc9-134">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-134">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3cfc9-135">-GlobalParameterDefinition</span><span class="sxs-lookup"><span data-stu-id="3cfc9-135">-GlobalParameterDefinition</span></span>
<span data-ttu-id="3cfc9-136">Dizionario che contiene i parametri globali della data factory.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-136">The dictionary containing the global parameters of the data factory.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cfc9-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="3cfc9-137">-HostName</span></span>
<span data-ttu-id="3cfc9-138">Nome host per la configurazione repo di GitHub.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-138">The host name for GitHub repo configuration.</span></span>

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

### <span data-ttu-id="3cfc9-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3cfc9-139">-InputObject</span></span>
<span data-ttu-id="3cfc9-140">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-140">The data factory object.</span></span>

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

### <span data-ttu-id="3cfc9-141">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="3cfc9-141">-LastCommitId</span></span>
<span data-ttu-id="3cfc9-142">L'ultimo ID commit per la configurazione di repo.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-142">The last commit id for repo configuration.</span></span>

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

### <span data-ttu-id="3cfc9-143">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3cfc9-143">-Location</span></span>
<span data-ttu-id="3cfc9-144">La factory di dati viene creata nell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-144">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="3cfc9-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="3cfc9-145">-Name</span></span>
<span data-ttu-id="3cfc9-146">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-146">The data factory name.</span></span>

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

### <span data-ttu-id="3cfc9-147">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="3cfc9-147">-ProjectName</span></span>
<span data-ttu-id="3cfc9-148">Il nome di progetto Azure DevOps per la configurazione di repo.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-148">The project name Azure DevOps for repo configuration.</span></span>

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

### <span data-ttu-id="3cfc9-149">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="3cfc9-149">-RepositoryName</span></span>
<span data-ttu-id="3cfc9-150">Nome del repository per la configurazione di repo.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-150">The repository name for repo configuration.</span></span>

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

### <span data-ttu-id="3cfc9-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cfc9-151">-ResourceGroupName</span></span>
<span data-ttu-id="3cfc9-152">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-152">The resource group name.</span></span>

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

### <span data-ttu-id="3cfc9-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cfc9-153">-ResourceId</span></span>
<span data-ttu-id="3cfc9-154">ID risorsa Azure di V2 Data Factory.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-154">The Azure resource ID of V2 data factory.</span></span>

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

### <span data-ttu-id="3cfc9-155">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="3cfc9-155">-RootFolder</span></span>
<span data-ttu-id="3cfc9-156">Cartella radice per la configurazione di repo.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-156">The root folder for repo configuration.</span></span>

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

### <span data-ttu-id="3cfc9-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="3cfc9-157">-Tag</span></span>
<span data-ttu-id="3cfc9-158">Tag della data factory.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-158">The tags of the data factory.</span></span>

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

### <span data-ttu-id="3cfc9-159">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="3cfc9-159">-TenantId</span></span>
<span data-ttu-id="3cfc9-160">ID tenant per la configurazione di repository di Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-160">The tenant id for Azure DevOps repo configuration.</span></span>

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

### <span data-ttu-id="3cfc9-161">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3cfc9-161">-Confirm</span></span>
<span data-ttu-id="3cfc9-162">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cfc9-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cfc9-163">-WhatIf</span></span>
<span data-ttu-id="3cfc9-164">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3cfc9-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cfc9-165">CommonParameters</span></span>
<span data-ttu-id="3cfc9-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cfc9-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cfc9-167">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cfc9-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cfc9-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3cfc9-168">INPUTS</span></span>

### <span data-ttu-id="3cfc9-169">System. String</span><span class="sxs-lookup"><span data-stu-id="3cfc9-169">System.String</span></span>

### <span data-ttu-id="3cfc9-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3cfc9-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="3cfc9-171">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3cfc9-171">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3cfc9-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3cfc9-172">OUTPUTS</span></span>

### <span data-ttu-id="3cfc9-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3cfc9-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="3cfc9-174">Note</span><span class="sxs-lookup"><span data-stu-id="3cfc9-174">NOTES</span></span>
<span data-ttu-id="3cfc9-175">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="3cfc9-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3cfc9-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3cfc9-176">RELATED LINKS</span></span>

[<span data-ttu-id="3cfc9-177">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3cfc9-177">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="3cfc9-178">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3cfc9-178">Remove-AzDataFactoryV2</span></span>]()
