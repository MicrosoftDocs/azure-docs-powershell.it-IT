---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: e09c2660f37a7b737d137c0907ff74ef9e39a5ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972365"
---
# <span data-ttu-id="d7b20-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d7b20-101">New-AzWebApp</span></span>

## <span data-ttu-id="d7b20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7b20-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b20-103">Crea un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="d7b20-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="d7b20-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7b20-104">SYNTAX</span></span>

### <span data-ttu-id="d7b20-105">SimpleParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d7b20-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7b20-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="d7b20-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7b20-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7b20-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7b20-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d7b20-108">DESCRIPTION</span></span>
<span data-ttu-id="d7b20-109">Il cmdlet **New-AzWebApp** crea un'app Web di Azure in un dato gruppo di risorse che usa il piano di servizio app e il data center specificati.</span><span class="sxs-lookup"><span data-stu-id="d7b20-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="d7b20-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7b20-110">EXAMPLES</span></span>

### <span data-ttu-id="d7b20-111">Esempio 1: Creare un'app Web</span><span class="sxs-lookup"><span data-stu-id="d7b20-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="d7b20-112">Questo comando crea un'app Web di Azure denominata ContosoSite nel gruppo di risorse esistente denominato Default-Web-WestUS nel data center Degli Stati Uniti occidentali.</span><span class="sxs-lookup"><span data-stu-id="d7b20-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="d7b20-113">Il comando usa un piano di servizio app esistente denominato ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="d7b20-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="d7b20-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7b20-114">PARAMETERS</span></span>

### <span data-ttu-id="d7b20-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d7b20-115">-AppServicePlan</span></span>
<span data-ttu-id="d7b20-116">Nome del piano di servizio app o ID del piano di servizio dell'app. Se una WebApp e un piano di servizio per app sono in gruppi di risorse diversi, usare l'ID al posto del nome.</span><span class="sxs-lookup"><span data-stu-id="d7b20-116">App Service Plan Name or App Service Plan Id. If a WebApp and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="d7b20-117">L'ID del piano di servizio app può essere recuperato usando: $asp = Get-AzAppServicePlan -ResourceGroup myRG -Name MyWebapp $asp.id restituisce l'ID del piano di servizio dell'app.</span><span class="sxs-lookup"><span data-stu-id="d7b20-117">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b20-118">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="d7b20-118">-AppSettingsOverrides</span></span>
<span data-ttu-id="d7b20-119">Nelle impostazioni dell'app viene eseguito l'override di HashTable</span><span class="sxs-lookup"><span data-stu-id="d7b20-119">App Settings Overrides HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b20-120">-AseName</span><span class="sxs-lookup"><span data-stu-id="d7b20-120">-AseName</span></span>
<span data-ttu-id="d7b20-121">Nome dell'ambiente del servizio app</span><span class="sxs-lookup"><span data-stu-id="d7b20-121">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b20-122">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7b20-122">-AseResourceGroupName</span></span>
<span data-ttu-id="d7b20-123">Nome del gruppo di risorse dell'ambiente del servizio app</span><span class="sxs-lookup"><span data-stu-id="d7b20-123">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b20-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7b20-124">-AsJob</span></span>
<span data-ttu-id="d7b20-125">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d7b20-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7b20-126">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="d7b20-126">-ContainerImageName</span></span>
<span data-ttu-id="d7b20-127">Container Image Name and optional tag, for example (image:tag)</span><span class="sxs-lookup"><span data-stu-id="d7b20-127">Container Image Name and optional tag, for example (image:tag)</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b20-128">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="d7b20-128">-ContainerRegistryPassword</span></span>
<span data-ttu-id="d7b20-129">Password del Registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="d7b20-129">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b20-130">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="d7b20-130">-ContainerRegistryUrl</span></span>
<span data-ttu-id="d7b20-131">Url del server del Registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="d7b20-131">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b20-132">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="d7b20-132">-ContainerRegistryUser</span></span>
<span data-ttu-id="d7b20-133">Nome utente del Registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="d7b20-133">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b20-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7b20-134">-DefaultProfile</span></span>
<span data-ttu-id="d7b20-135">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d7b20-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7b20-136">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="d7b20-136">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="d7b20-137">Webhook di distribuzione continua contenitore/disabilita</span><span class="sxs-lookup"><span data-stu-id="d7b20-137">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="d7b20-138">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="d7b20-138">-GitRepositoryPath</span></span>
<span data-ttu-id="d7b20-139">Percorso del repository GitHub che contiene l'applicazione Web da distribuire.</span><span class="sxs-lookup"><span data-stu-id="d7b20-139">Path to the GitHub repository containing the web application to deploy.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b20-140">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="d7b20-140">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="d7b20-141">Opzione Ignora nomi host personalizzati</span><span class="sxs-lookup"><span data-stu-id="d7b20-141">Ignore Custom Host Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b20-142">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="d7b20-142">-IgnoreSourceControl</span></span>
<span data-ttu-id="d7b20-143">Opzione Ignora controllo origine</span><span class="sxs-lookup"><span data-stu-id="d7b20-143">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b20-144">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="d7b20-144">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="d7b20-145">Opzione Includi slot WebApp di origine</span><span class="sxs-lookup"><span data-stu-id="d7b20-145">Include Source WebApp Slots Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b20-146">-Location</span><span class="sxs-lookup"><span data-stu-id="d7b20-146">-Location</span></span>
<span data-ttu-id="d7b20-147">Posizione</span><span class="sxs-lookup"><span data-stu-id="d7b20-147">Location</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, PrivateRegistry
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b20-148">-Name</span><span class="sxs-lookup"><span data-stu-id="d7b20-148">-Name</span></span>
<span data-ttu-id="d7b20-149">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="d7b20-149">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebAppName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b20-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7b20-150">-ResourceGroupName</span></span>
<span data-ttu-id="d7b20-151">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d7b20-151">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PrivateRegistry, WebAppParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b20-152">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="d7b20-152">-SourceWebApp</span></span>
<span data-ttu-id="d7b20-153">Oggetto WebApp di origine</span><span class="sxs-lookup"><span data-stu-id="d7b20-153">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b20-154">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d7b20-154">-TrafficManagerProfile</span></span>
<span data-ttu-id="d7b20-155">ID risorsa del profilo di Gestore traffico esistente</span><span class="sxs-lookup"><span data-stu-id="d7b20-155">Resource Id of existing traffic manager profile</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases: TrafficManagerProfileName, TrafficManagerProfileId

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b20-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7b20-156">-Confirm</span></span>
<span data-ttu-id="d7b20-157">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7b20-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7b20-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7b20-158">-WhatIf</span></span>
<span data-ttu-id="d7b20-159">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7b20-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7b20-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7b20-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7b20-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b20-161">CommonParameters</span></span>
<span data-ttu-id="d7b20-162">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7b20-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b20-163">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7b20-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b20-164">INPUT</span><span class="sxs-lookup"><span data-stu-id="d7b20-164">INPUTS</span></span>

### <span data-ttu-id="d7b20-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="d7b20-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d7b20-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7b20-166">OUTPUTS</span></span>

### <span data-ttu-id="d7b20-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="d7b20-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d7b20-168">NOTE</span><span class="sxs-lookup"><span data-stu-id="d7b20-168">NOTES</span></span>

## <span data-ttu-id="d7b20-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7b20-169">RELATED LINKS</span></span>

[<span data-ttu-id="d7b20-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d7b20-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="d7b20-171">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d7b20-171">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="d7b20-172">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d7b20-172">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="d7b20-173">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d7b20-173">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="d7b20-174">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d7b20-174">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


