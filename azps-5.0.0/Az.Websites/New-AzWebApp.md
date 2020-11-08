---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: 760aacba880276059c4a468454cccec29d397183
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200054"
---
# <span data-ttu-id="971e7-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="971e7-101">New-AzWebApp</span></span>

## <span data-ttu-id="971e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="971e7-102">SYNOPSIS</span></span>
<span data-ttu-id="971e7-103">Crea un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="971e7-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="971e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="971e7-104">SYNTAX</span></span>

### <span data-ttu-id="971e7-105">SimpleParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="971e7-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="971e7-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="971e7-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="971e7-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="971e7-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="971e7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="971e7-108">DESCRIPTION</span></span>
<span data-ttu-id="971e7-109">Il cmdlet **New-AzWebApp** crea un'app Web di Azure in un gruppo di risorse specificato che usa il piano di servizio app e il Data Center specificati.</span><span class="sxs-lookup"><span data-stu-id="971e7-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="971e7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="971e7-110">EXAMPLES</span></span>

### <span data-ttu-id="971e7-111">Esempio 1: creare un'app Web</span><span class="sxs-lookup"><span data-stu-id="971e7-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="971e7-112">Questo comando crea un'app Web di Azure denominata ContosoSite nel gruppo di risorse esistente denominato Default-Web-Westus nel Data Center West US.</span><span class="sxs-lookup"><span data-stu-id="971e7-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="971e7-113">Il comando usa un piano di servizio app esistente denominato ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="971e7-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="971e7-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="971e7-114">PARAMETERS</span></span>

### <span data-ttu-id="971e7-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="971e7-115">-AppServicePlan</span></span>
<span data-ttu-id="971e7-116">Nome piano servizio app o ID piano servizio app. Se un piano di servizio Web App e app si trova in gruppi di risorse diversi, usare l'ID al posto del nome.</span><span class="sxs-lookup"><span data-stu-id="971e7-116">App Service Plan Name or App Service Plan Id. If a WebApp and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="971e7-117">L'ID piano di servizio app può essere recuperato usando: $asp = Get-AzAppServicePlan-ResourceGroup myRG-Name MyWebapp $asp. ID restituisce l'ID del piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="971e7-117">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>


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

### <span data-ttu-id="971e7-118">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="971e7-118">-AppSettingsOverrides</span></span>
<span data-ttu-id="971e7-119">Le impostazioni dell'app vengono sostituite da HashTable</span><span class="sxs-lookup"><span data-stu-id="971e7-119">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="971e7-120">-AseName</span><span class="sxs-lookup"><span data-stu-id="971e7-120">-AseName</span></span>
<span data-ttu-id="971e7-121">Nome ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="971e7-121">App Service Environment Name</span></span>

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

### <span data-ttu-id="971e7-122">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="971e7-122">-AseResourceGroupName</span></span>
<span data-ttu-id="971e7-123">Nome del gruppo risorse ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="971e7-123">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="971e7-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="971e7-124">-AsJob</span></span>
<span data-ttu-id="971e7-125">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="971e7-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="971e7-126">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="971e7-126">-ContainerImageName</span></span>
<span data-ttu-id="971e7-127">Nome immagine contenitore e tag facoltativo, ad esempio (immagine: Tag)</span><span class="sxs-lookup"><span data-stu-id="971e7-127">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="971e7-128">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="971e7-128">-ContainerRegistryPassword</span></span>
<span data-ttu-id="971e7-129">Password del registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="971e7-129">Private Container Registry Password</span></span>

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

### <span data-ttu-id="971e7-130">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="971e7-130">-ContainerRegistryUrl</span></span>
<span data-ttu-id="971e7-131">URL del server del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="971e7-131">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="971e7-132">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="971e7-132">-ContainerRegistryUser</span></span>
<span data-ttu-id="971e7-133">Nome utente del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="971e7-133">Private Container Registry Username</span></span>

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

### <span data-ttu-id="971e7-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="971e7-134">-DefaultProfile</span></span>
<span data-ttu-id="971e7-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="971e7-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="971e7-136">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="971e7-136">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="971e7-137">Abilita/Disabilita il webhook di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="971e7-137">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="971e7-138">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="971e7-138">-GitRepositoryPath</span></span>
<span data-ttu-id="971e7-139">Percorso del repository GitHub che contiene l'applicazione Web da distribuire.</span><span class="sxs-lookup"><span data-stu-id="971e7-139">Path to the GitHub repository containing the web application to deploy.</span></span>

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

### <span data-ttu-id="971e7-140">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="971e7-140">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="971e7-141">Opzione Ignora nomi host personalizzati</span><span class="sxs-lookup"><span data-stu-id="971e7-141">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="971e7-142">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="971e7-142">-IgnoreSourceControl</span></span>
<span data-ttu-id="971e7-143">Opzione Ignora controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="971e7-143">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="971e7-144">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="971e7-144">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="971e7-145">Opzione Includi slot web app di origine</span><span class="sxs-lookup"><span data-stu-id="971e7-145">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="971e7-146">-Posizione</span><span class="sxs-lookup"><span data-stu-id="971e7-146">-Location</span></span>
<span data-ttu-id="971e7-147">Posizione</span><span class="sxs-lookup"><span data-stu-id="971e7-147">Location</span></span>

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

### <span data-ttu-id="971e7-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="971e7-148">-Name</span></span>
<span data-ttu-id="971e7-149">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="971e7-149">WebApp Name</span></span>

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

### <span data-ttu-id="971e7-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="971e7-150">-ResourceGroupName</span></span>
<span data-ttu-id="971e7-151">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="971e7-151">Resource Group Name</span></span>

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

### <span data-ttu-id="971e7-152">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="971e7-152">-SourceWebApp</span></span>
<span data-ttu-id="971e7-153">Oggetto Web App di origine</span><span class="sxs-lookup"><span data-stu-id="971e7-153">Source WebApp Object</span></span>

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

### <span data-ttu-id="971e7-154">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="971e7-154">-TrafficManagerProfile</span></span>
<span data-ttu-id="971e7-155">ID risorsa del profilo di gestione traffico esistente</span><span class="sxs-lookup"><span data-stu-id="971e7-155">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="971e7-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="971e7-156">-Confirm</span></span>
<span data-ttu-id="971e7-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="971e7-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="971e7-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="971e7-158">-WhatIf</span></span>
<span data-ttu-id="971e7-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="971e7-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="971e7-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="971e7-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="971e7-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="971e7-161">CommonParameters</span></span>
<span data-ttu-id="971e7-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="971e7-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="971e7-163">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="971e7-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="971e7-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="971e7-164">INPUTS</span></span>

### <span data-ttu-id="971e7-165">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="971e7-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="971e7-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="971e7-166">OUTPUTS</span></span>

### <span data-ttu-id="971e7-167">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="971e7-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="971e7-168">Note</span><span class="sxs-lookup"><span data-stu-id="971e7-168">NOTES</span></span>

## <span data-ttu-id="971e7-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="971e7-169">RELATED LINKS</span></span>

[<span data-ttu-id="971e7-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="971e7-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="971e7-171">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="971e7-171">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="971e7-172">Riavviare-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="971e7-172">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="971e7-173">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="971e7-173">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="971e7-174">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="971e7-174">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


