---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 374263c26a3572e8d85e18d1795c27a761866a4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674930"
---
# <span data-ttu-id="ff72a-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ff72a-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="ff72a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff72a-102">SYNOPSIS</span></span>
<span data-ttu-id="ff72a-103">Crea una data factory.</span><span class="sxs-lookup"><span data-stu-id="ff72a-103">Creates a data factory.</span></span>

## <span data-ttu-id="ff72a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff72a-104">SYNTAX</span></span>

### <span data-ttu-id="ff72a-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ff72a-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff72a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ff72a-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff72a-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="ff72a-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff72a-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="ff72a-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff72a-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="ff72a-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff72a-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="ff72a-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff72a-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ff72a-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff72a-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="ff72a-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff72a-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="ff72a-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff72a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff72a-114">DESCRIPTION</span></span>
<span data-ttu-id="ff72a-115">Il cmdlet **set-AzDataFactoryV2** crea una factory di dati con il nome e il percorso del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="ff72a-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="ff72a-116">Eseguire queste operazioni nell'ordine seguente:--creare una factory di dati.</span><span class="sxs-lookup"><span data-stu-id="ff72a-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="ff72a-117">--Creare servizi collegati.</span><span class="sxs-lookup"><span data-stu-id="ff72a-117">-- Create linked services.</span></span>
<span data-ttu-id="ff72a-118">--Creare DataSet.</span><span class="sxs-lookup"><span data-stu-id="ff72a-118">-- Create datasets.</span></span>
<span data-ttu-id="ff72a-119">--Crea una pipeline.</span><span class="sxs-lookup"><span data-stu-id="ff72a-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="ff72a-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff72a-120">EXAMPLES</span></span>

### <span data-ttu-id="ff72a-121">Esempio 1: creare una data factory</span><span class="sxs-lookup"><span data-stu-id="ff72a-121">Example 1: Create a data factory</span></span>
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

### <span data-ttu-id="ff72a-122">Esempio 2: creare una factory di dati con i dettagli di repoconfiguration usando un oggetto factory esistente.</span><span class="sxs-lookup"><span data-stu-id="ff72a-122">Example 2: Create a data factory with repoconfiguration details using an existing factory object.</span></span>
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

<span data-ttu-id="ff72a-123">Questo comando crea una factory di dati denominata WikiADF nel gruppo di risorse denominato ADF nella posizione Westus.</span><span class="sxs-lookup"><span data-stu-id="ff72a-123">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="ff72a-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff72a-124">PARAMETERS</span></span>

### <span data-ttu-id="ff72a-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ff72a-125">-AccountName</span></span>
<span data-ttu-id="ff72a-126">Nome dell'account per la configurazione di repo.</span><span class="sxs-lookup"><span data-stu-id="ff72a-126">The account name for repo configuration.</span></span>

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

### <span data-ttu-id="ff72a-127">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="ff72a-127">-CollaborationBranch</span></span>
<span data-ttu-id="ff72a-128">Ramo collaborazione per la configurazione dei repo.</span><span class="sxs-lookup"><span data-stu-id="ff72a-128">The collaboration branch for repo configuration.</span></span>

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

### <span data-ttu-id="ff72a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff72a-129">-DefaultProfile</span></span>
<span data-ttu-id="ff72a-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff72a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff72a-131">-Force</span><span class="sxs-lookup"><span data-stu-id="ff72a-131">-Force</span></span>
<span data-ttu-id="ff72a-132">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ff72a-132">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ff72a-133">-HostName</span><span class="sxs-lookup"><span data-stu-id="ff72a-133">-HostName</span></span>
<span data-ttu-id="ff72a-134">Nome host per la configurazione di repo.</span><span class="sxs-lookup"><span data-stu-id="ff72a-134">The host name for repo configuration.</span></span>

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

### <span data-ttu-id="ff72a-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff72a-135">-InputObject</span></span>
<span data-ttu-id="ff72a-136">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ff72a-136">The data factory object.</span></span>

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

### <span data-ttu-id="ff72a-137">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="ff72a-137">-LastCommitId</span></span>
<span data-ttu-id="ff72a-138">L'ultimo ID commit per la configurazione di repo.</span><span class="sxs-lookup"><span data-stu-id="ff72a-138">The last commit id for repo configuration.</span></span>

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

### <span data-ttu-id="ff72a-139">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ff72a-139">-Location</span></span>
<span data-ttu-id="ff72a-140">La factory di dati viene creata nell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="ff72a-140">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="ff72a-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff72a-141">-Name</span></span>
<span data-ttu-id="ff72a-142">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="ff72a-142">The data factory name.</span></span>

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

### <span data-ttu-id="ff72a-143">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="ff72a-143">-ProjectName</span></span>
<span data-ttu-id="ff72a-144">Nome del progetto per la configurazione di repo.</span><span class="sxs-lookup"><span data-stu-id="ff72a-144">The project name for repo configuration.</span></span>

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

### <span data-ttu-id="ff72a-145">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="ff72a-145">-RepositoryName</span></span>
<span data-ttu-id="ff72a-146">Nome del repository per la configurazione di repo.</span><span class="sxs-lookup"><span data-stu-id="ff72a-146">The repository name for repo configuration.</span></span>

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

### <span data-ttu-id="ff72a-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff72a-147">-ResourceGroupName</span></span>
<span data-ttu-id="ff72a-148">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ff72a-148">The resource group name.</span></span>

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

### <span data-ttu-id="ff72a-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff72a-149">-ResourceId</span></span>
<span data-ttu-id="ff72a-150">ID risorsa Azure di V2 Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ff72a-150">The Azure resource ID of V2 data factory.</span></span>

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

### <span data-ttu-id="ff72a-151">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="ff72a-151">-RootFolder</span></span>
<span data-ttu-id="ff72a-152">Cartella radice per la configurazione di repo.</span><span class="sxs-lookup"><span data-stu-id="ff72a-152">The root folder for repo configuration.</span></span>

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

### <span data-ttu-id="ff72a-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="ff72a-153">-Tag</span></span>
<span data-ttu-id="ff72a-154">Tag della data factory.</span><span class="sxs-lookup"><span data-stu-id="ff72a-154">The tags of the data factory.</span></span>

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

### <span data-ttu-id="ff72a-155">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="ff72a-155">-TenantId</span></span>
<span data-ttu-id="ff72a-156">ID tenant per la configurazione dei repo.</span><span class="sxs-lookup"><span data-stu-id="ff72a-156">The tenant id for repo configuration.</span></span>

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

### <span data-ttu-id="ff72a-157">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ff72a-157">-Confirm</span></span>
<span data-ttu-id="ff72a-158">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff72a-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff72a-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff72a-159">-WhatIf</span></span>
<span data-ttu-id="ff72a-160">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff72a-160">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ff72a-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff72a-161">CommonParameters</span></span>
<span data-ttu-id="ff72a-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff72a-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff72a-163">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff72a-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff72a-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff72a-164">INPUTS</span></span>

### <span data-ttu-id="ff72a-165">System. String</span><span class="sxs-lookup"><span data-stu-id="ff72a-165">System.String</span></span>

### <span data-ttu-id="ff72a-166">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ff72a-166">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ff72a-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff72a-167">OUTPUTS</span></span>

### <span data-ttu-id="ff72a-168">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ff72a-168">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="ff72a-169">Note</span><span class="sxs-lookup"><span data-stu-id="ff72a-169">NOTES</span></span>
<span data-ttu-id="ff72a-170">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="ff72a-170">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ff72a-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff72a-171">RELATED LINKS</span></span>

[<span data-ttu-id="ff72a-172">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ff72a-172">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="ff72a-173">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ff72a-173">Remove-AzDataFactoryV2</span></span>]()
