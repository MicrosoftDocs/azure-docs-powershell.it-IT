---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 4948de891815345efdc0b3f4ec39fb1874e510b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521504"
---
# <span data-ttu-id="31ec8-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="31ec8-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="31ec8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31ec8-102">SYNOPSIS</span></span>
<span data-ttu-id="31ec8-103">Crea un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="31ec8-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31ec8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31ec8-104">SYNTAX</span></span>

### <span data-ttu-id="31ec8-105">S1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="31ec8-105">S1 (Default)</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [[-TrafficManagerProfileId] <String>]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31ec8-106">S2</span><span class="sxs-lookup"><span data-stu-id="31ec8-106">S2</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [[-TrafficManagerProfileName] <String>]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31ec8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31ec8-107">DESCRIPTION</span></span>
<span data-ttu-id="31ec8-108">Il cmdlet **New-AzureRmWebApp** crea un'app Web di Azure in un gruppo di risorse specificato che usa il piano di servizio app e il Data Center specificati.</span><span class="sxs-lookup"><span data-stu-id="31ec8-108">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="31ec8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31ec8-109">EXAMPLES</span></span>

### <span data-ttu-id="31ec8-110">Esempio 1: creare un'app Web</span><span class="sxs-lookup"><span data-stu-id="31ec8-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="31ec8-111">Questo comando crea un'app Web di Azure denominata ContosoSite nel gruppo di risorse esistente denominato Default-Web-Westus nel Data Center West US.</span><span class="sxs-lookup"><span data-stu-id="31ec8-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="31ec8-112">Il comando usa un piano di servizio app esistente denominato ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="31ec8-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="31ec8-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31ec8-113">PARAMETERS</span></span>

### <span data-ttu-id="31ec8-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="31ec8-114">-AppServicePlan</span></span>
<span data-ttu-id="31ec8-115">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="31ec8-115">App Service Plan Name</span></span>

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

### <span data-ttu-id="31ec8-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="31ec8-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="31ec8-117">Le impostazioni dell'app vengono sostituite da HashTable</span><span class="sxs-lookup"><span data-stu-id="31ec8-117">App Settings Overrides HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ec8-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="31ec8-118">-AseName</span></span>
<span data-ttu-id="31ec8-119">Nome ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="31ec8-119">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ec8-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31ec8-120">-AseResourceGroupName</span></span>
<span data-ttu-id="31ec8-121">Nome del gruppo risorse ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="31ec8-121">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ec8-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="31ec8-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="31ec8-123">Opzione Ignora nomi host personalizzati</span><span class="sxs-lookup"><span data-stu-id="31ec8-123">Ignore Custom Host Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ec8-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="31ec8-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="31ec8-125">Opzione Ignora controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="31ec8-125">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ec8-126">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="31ec8-126">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="31ec8-127">Opzione Includi slot web app di origine</span><span class="sxs-lookup"><span data-stu-id="31ec8-127">Include Source WebApp Slots Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ec8-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="31ec8-128">-Location</span></span>
<span data-ttu-id="31ec8-129">Posizione</span><span class="sxs-lookup"><span data-stu-id="31ec8-129">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ec8-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="31ec8-130">-Name</span></span>
<span data-ttu-id="31ec8-131">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="31ec8-131">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ec8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31ec8-132">-ResourceGroupName</span></span>
<span data-ttu-id="31ec8-133">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="31ec8-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ec8-134">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="31ec8-134">-SourceWebApp</span></span>
<span data-ttu-id="31ec8-135">Oggetto Web App di origine</span><span class="sxs-lookup"><span data-stu-id="31ec8-135">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31ec8-136">-TrafficManagerProfileId</span><span class="sxs-lookup"><span data-stu-id="31ec8-136">-TrafficManagerProfileId</span></span>
<span data-ttu-id="31ec8-137">ID profilo di gestione traffico</span><span class="sxs-lookup"><span data-stu-id="31ec8-137">Traffic Manager Profile Id</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ec8-138">-TrafficManagerProfileName</span><span class="sxs-lookup"><span data-stu-id="31ec8-138">-TrafficManagerProfileName</span></span>
<span data-ttu-id="31ec8-139">Nome del profilo di Traffic Manager</span><span class="sxs-lookup"><span data-stu-id="31ec8-139">Traffic Manager Profile Name</span></span>

```yaml
Type: System.String
Parameter Sets: S2
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ec8-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ec8-140">-DefaultProfile</span></span>
<span data-ttu-id="31ec8-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31ec8-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31ec8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ec8-142">CommonParameters</span></span>
<span data-ttu-id="31ec8-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31ec8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ec8-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31ec8-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ec8-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31ec8-145">INPUTS</span></span>

### <span data-ttu-id="31ec8-146">Sito</span><span class="sxs-lookup"><span data-stu-id="31ec8-146">Site</span></span>
<span data-ttu-id="31ec8-147">Il parametro "SourceWebApp" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="31ec8-147">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="31ec8-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31ec8-148">OUTPUTS</span></span>

## <span data-ttu-id="31ec8-149">Note</span><span class="sxs-lookup"><span data-stu-id="31ec8-149">NOTES</span></span>

## <span data-ttu-id="31ec8-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31ec8-150">RELATED LINKS</span></span>

[<span data-ttu-id="31ec8-151">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="31ec8-151">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="31ec8-152">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="31ec8-152">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="31ec8-153">Riavviare-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="31ec8-153">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="31ec8-154">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="31ec8-154">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="31ec8-155">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="31ec8-155">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


