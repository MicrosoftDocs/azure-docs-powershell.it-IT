---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: 03aca295edc9a0c7d1a2b2bde7a78419158209dc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865869"
---
# <span data-ttu-id="7e19d-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7e19d-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="7e19d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e19d-102">SYNOPSIS</span></span>
<span data-ttu-id="7e19d-103">Crea un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="7e19d-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e19d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e19d-104">SYNTAX</span></span>

### <span data-ttu-id="7e19d-105">SimpleParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7e19d-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-AsJob] [-GitRepositoryPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e19d-106">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e19d-106">WebAppParameterSet</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [-SourceWebApp] <Site> [[-TrafficManagerProfile] <String>] [-IgnoreSourceControl]
 [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e19d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e19d-107">DESCRIPTION</span></span>
<span data-ttu-id="7e19d-108">Il cmdlet **New-AzureRmWebApp** crea un'app Web di Azure in un gruppo di risorse specificato che usa il piano di servizio app e il Data Center specificati.</span><span class="sxs-lookup"><span data-stu-id="7e19d-108">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="7e19d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e19d-109">EXAMPLES</span></span>

### <span data-ttu-id="7e19d-110">Esempio 1: creare un'app Web</span><span class="sxs-lookup"><span data-stu-id="7e19d-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="7e19d-111">Questo comando crea un'app Web di Azure denominata ContosoSite nel gruppo di risorse esistente denominato Default-Web-Westus nel Data Center West US.</span><span class="sxs-lookup"><span data-stu-id="7e19d-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="7e19d-112">Il comando usa un piano di servizio app esistente denominato ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="7e19d-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="7e19d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e19d-113">PARAMETERS</span></span>

### <span data-ttu-id="7e19d-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7e19d-114">-AppServicePlan</span></span>
<span data-ttu-id="7e19d-115">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="7e19d-115">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e19d-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="7e19d-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="7e19d-117">Le impostazioni dell'app vengono sostituite da HashTable</span><span class="sxs-lookup"><span data-stu-id="7e19d-117">App Settings Overrides HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e19d-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="7e19d-118">-AseName</span></span>
<span data-ttu-id="7e19d-119">Nome ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="7e19d-119">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e19d-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e19d-120">-AseResourceGroupName</span></span>
<span data-ttu-id="7e19d-121">Nome del gruppo risorse ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="7e19d-121">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e19d-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e19d-122">-AsJob</span></span>
<span data-ttu-id="7e19d-123">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7e19d-123">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e19d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e19d-124">-DefaultProfile</span></span>
<span data-ttu-id="7e19d-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e19d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e19d-126">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="7e19d-126">-GitRepositoryPath</span></span>
<span data-ttu-id="7e19d-127">Percorso del repository GitHub containign l'applicazione Web da distribuire.</span><span class="sxs-lookup"><span data-stu-id="7e19d-127">Path to the GitHub repository containign the web application to deploy.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e19d-128">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="7e19d-128">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="7e19d-129">Opzione Ignora nomi host personalizzati</span><span class="sxs-lookup"><span data-stu-id="7e19d-129">Ignore Custom Host Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e19d-130">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="7e19d-130">-IgnoreSourceControl</span></span>
<span data-ttu-id="7e19d-131">Opzione Ignora controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="7e19d-131">Ignore Source Control Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e19d-132">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="7e19d-132">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="7e19d-133">Opzione Includi slot web app di origine</span><span class="sxs-lookup"><span data-stu-id="7e19d-133">Include Source WebApp Slots Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e19d-134">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7e19d-134">-Location</span></span>
<span data-ttu-id="7e19d-135">Posizione</span><span class="sxs-lookup"><span data-stu-id="7e19d-135">Location</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e19d-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e19d-136">-Name</span></span>
<span data-ttu-id="7e19d-137">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="7e19d-137">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebAppName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e19d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e19d-138">-ResourceGroupName</span></span>
<span data-ttu-id="7e19d-139">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="7e19d-139">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e19d-140">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="7e19d-140">-SourceWebApp</span></span>
<span data-ttu-id="7e19d-141">Oggetto Web App di origine</span><span class="sxs-lookup"><span data-stu-id="7e19d-141">Source WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e19d-142">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e19d-142">-TrafficManagerProfile</span></span>
<span data-ttu-id="7e19d-143">ID risorsa del profilo di gestione traffico esistente</span><span class="sxs-lookup"><span data-stu-id="7e19d-143">Resource Id of existing traffic manager profile</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: TrafficManagerProfileName, TrafficManagerProfileId

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e19d-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7e19d-144">-Confirm</span></span>
<span data-ttu-id="7e19d-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e19d-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e19d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e19d-146">-WhatIf</span></span>
<span data-ttu-id="7e19d-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e19d-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e19d-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e19d-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e19d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e19d-149">CommonParameters</span></span>
<span data-ttu-id="7e19d-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e19d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e19d-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e19d-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e19d-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e19d-152">INPUTS</span></span>

### <span data-ttu-id="7e19d-153">Sito</span><span class="sxs-lookup"><span data-stu-id="7e19d-153">Site</span></span>
<span data-ttu-id="7e19d-154">Il parametro "SourceWebApp" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7e19d-154">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7e19d-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e19d-155">OUTPUTS</span></span>

### <span data-ttu-id="7e19d-156">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="7e19d-156">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="7e19d-157">Note</span><span class="sxs-lookup"><span data-stu-id="7e19d-157">NOTES</span></span>

## <span data-ttu-id="7e19d-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e19d-158">RELATED LINKS</span></span>

[<span data-ttu-id="7e19d-159">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7e19d-159">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="7e19d-160">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7e19d-160">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="7e19d-161">Riavviare-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7e19d-161">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="7e19d-162">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7e19d-162">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="7e19d-163">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7e19d-163">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


