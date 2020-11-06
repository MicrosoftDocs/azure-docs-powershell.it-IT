---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 2dfa72867655b95ea752c23c8605f19e7544e8e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507243"
---
# <span data-ttu-id="38a18-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="38a18-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="38a18-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38a18-102">SYNOPSIS</span></span>
<span data-ttu-id="38a18-103">Crea un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="38a18-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38a18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38a18-104">SYNTAX</span></span>

### <span data-ttu-id="38a18-105">SimpleParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="38a18-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38a18-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="38a18-106">PrivateRegistry</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] -ContainerImageName <String> -ContainerRegistryUrl <String>
 -ContainerRegistryUser <String> -ContainerRegistryPassword <SecureString>
 [-EnableContainerContinuousDeployment] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38a18-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="38a18-107">WebAppParameterSet</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>]
 [-EnableContainerContinuousDeployment] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-IncludeSourceWebAppSlots] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38a18-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38a18-108">DESCRIPTION</span></span>
<span data-ttu-id="38a18-109">Il cmdlet **New-AzureRmWebApp** crea un'app Web di Azure in un gruppo di risorse specificato che usa il piano di servizio app e il Data Center specificati.</span><span class="sxs-lookup"><span data-stu-id="38a18-109">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="38a18-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38a18-110">EXAMPLES</span></span>

### <span data-ttu-id="38a18-111">Esempio 1: creare un'app Web</span><span class="sxs-lookup"><span data-stu-id="38a18-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="38a18-112">Questo comando crea un'app Web di Azure denominata ContosoSite nel gruppo di risorse esistente denominato Default-Web-Westus nel Data Center West US.</span><span class="sxs-lookup"><span data-stu-id="38a18-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="38a18-113">Il comando usa un piano di servizio app esistente denominato ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="38a18-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="38a18-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38a18-114">PARAMETERS</span></span>

### <span data-ttu-id="38a18-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="38a18-115">-AppServicePlan</span></span>
<span data-ttu-id="38a18-116">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="38a18-116">App Service Plan Name</span></span>

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

### <span data-ttu-id="38a18-117">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="38a18-117">-AppSettingsOverrides</span></span>
<span data-ttu-id="38a18-118">Le impostazioni dell'app vengono sostituite da HashTable</span><span class="sxs-lookup"><span data-stu-id="38a18-118">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="38a18-119">-AseName</span><span class="sxs-lookup"><span data-stu-id="38a18-119">-AseName</span></span>
<span data-ttu-id="38a18-120">Nome ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="38a18-120">App Service Environment Name</span></span>

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

### <span data-ttu-id="38a18-121">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38a18-121">-AseResourceGroupName</span></span>
<span data-ttu-id="38a18-122">Nome del gruppo risorse ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="38a18-122">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="38a18-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38a18-123">-AsJob</span></span>
<span data-ttu-id="38a18-124">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="38a18-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38a18-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="38a18-125">-ContainerImageName</span></span>
<span data-ttu-id="38a18-126">Nome immagine contenitore e tag facoltativo, ad esempio (immagine: Tag)</span><span class="sxs-lookup"><span data-stu-id="38a18-126">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="38a18-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="38a18-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="38a18-128">Password del registro di sistema del contenitore privato</span><span class="sxs-lookup"><span data-stu-id="38a18-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="38a18-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="38a18-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="38a18-130">URL del server del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="38a18-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="38a18-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="38a18-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="38a18-132">Nome utente del registro di sistema privato</span><span class="sxs-lookup"><span data-stu-id="38a18-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="38a18-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a18-133">-DefaultProfile</span></span>
<span data-ttu-id="38a18-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38a18-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a18-135">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="38a18-135">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="38a18-136">Abilita/Disabilita il webhook di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="38a18-136">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="38a18-137">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="38a18-137">-GitRepositoryPath</span></span>
<span data-ttu-id="38a18-138">Percorso del repository GitHub containign l'applicazione Web da distribuire.</span><span class="sxs-lookup"><span data-stu-id="38a18-138">Path to the GitHub repository containign the web application to deploy.</span></span>

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

### <span data-ttu-id="38a18-139">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="38a18-139">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="38a18-140">Opzione Ignora nomi host personalizzati</span><span class="sxs-lookup"><span data-stu-id="38a18-140">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="38a18-141">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="38a18-141">-IgnoreSourceControl</span></span>
<span data-ttu-id="38a18-142">Opzione Ignora controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="38a18-142">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="38a18-143">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="38a18-143">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="38a18-144">Opzione Includi slot web app di origine</span><span class="sxs-lookup"><span data-stu-id="38a18-144">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="38a18-145">-Posizione</span><span class="sxs-lookup"><span data-stu-id="38a18-145">-Location</span></span>
<span data-ttu-id="38a18-146">Posizione</span><span class="sxs-lookup"><span data-stu-id="38a18-146">Location</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, PrivateRegistry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a18-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="38a18-147">-Name</span></span>
<span data-ttu-id="38a18-148">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="38a18-148">WebApp Name</span></span>

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

### <span data-ttu-id="38a18-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38a18-149">-ResourceGroupName</span></span>
<span data-ttu-id="38a18-150">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="38a18-150">Resource Group Name</span></span>

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

### <span data-ttu-id="38a18-151">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="38a18-151">-SourceWebApp</span></span>
<span data-ttu-id="38a18-152">Oggetto Web App di origine</span><span class="sxs-lookup"><span data-stu-id="38a18-152">Source WebApp Object</span></span>

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

### <span data-ttu-id="38a18-153">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="38a18-153">-TrafficManagerProfile</span></span>
<span data-ttu-id="38a18-154">ID risorsa del profilo di gestione traffico esistente</span><span class="sxs-lookup"><span data-stu-id="38a18-154">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="38a18-155">-Confermare</span><span class="sxs-lookup"><span data-stu-id="38a18-155">-Confirm</span></span>
<span data-ttu-id="38a18-156">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38a18-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38a18-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38a18-157">-WhatIf</span></span>
<span data-ttu-id="38a18-158">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38a18-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38a18-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38a18-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38a18-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a18-160">CommonParameters</span></span>
<span data-ttu-id="38a18-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38a18-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a18-162">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38a18-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a18-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38a18-163">INPUTS</span></span>

### <span data-ttu-id="38a18-164">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="38a18-164">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="38a18-165">Parametri: SourceWebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="38a18-165">Parameters: SourceWebApp (ByValue)</span></span>

## <span data-ttu-id="38a18-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38a18-166">OUTPUTS</span></span>

### <span data-ttu-id="38a18-167">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="38a18-167">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="38a18-168">Note</span><span class="sxs-lookup"><span data-stu-id="38a18-168">NOTES</span></span>

## <span data-ttu-id="38a18-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38a18-169">RELATED LINKS</span></span>

[<span data-ttu-id="38a18-170">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="38a18-170">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="38a18-171">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="38a18-171">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="38a18-172">Riavviare-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="38a18-172">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="38a18-173">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="38a18-173">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="38a18-174">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="38a18-174">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


