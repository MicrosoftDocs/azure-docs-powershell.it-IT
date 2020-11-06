---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
ms.openlocfilehash: 3e886803ff608522bd2d563dd9b6cd6effcfe074
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521496"
---
# <span data-ttu-id="fbd31-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fbd31-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="fbd31-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fbd31-102">SYNOPSIS</span></span>
<span data-ttu-id="fbd31-103">Crea uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="fbd31-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbd31-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fbd31-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbd31-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbd31-105">DESCRIPTION</span></span>
<span data-ttu-id="fbd31-106">Il cmdlet **New-AzureRmWebAppSlot** crea uno slot di Azure Web App in un determinato gruppo di risorse che usa il piano di servizio app e il Data Center specificati.</span><span class="sxs-lookup"><span data-stu-id="fbd31-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="fbd31-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fbd31-107">EXAMPLES</span></span>

### <span data-ttu-id="fbd31-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fbd31-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="fbd31-109">Questo comando crea uno slot denominato Slot001 in un nome di app Web esistente ContosoSite nel gruppo di risorse esistente denominato Default-Web-Westus nel Data Center West US.</span><span class="sxs-lookup"><span data-stu-id="fbd31-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="fbd31-110">Il comando usa un piano di servizio app esistente denominato ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="fbd31-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="fbd31-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fbd31-111">PARAMETERS</span></span>

### <span data-ttu-id="fbd31-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fbd31-112">-AppServicePlan</span></span>
<span data-ttu-id="fbd31-113">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="fbd31-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="fbd31-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="fbd31-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="fbd31-115">Le impostazioni dell'app vengono sostituite da Hashtable</span><span class="sxs-lookup"><span data-stu-id="fbd31-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="fbd31-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="fbd31-116">-AseName</span></span>
<span data-ttu-id="fbd31-117">Nome ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="fbd31-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="fbd31-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbd31-118">-AseResourceGroupName</span></span>
<span data-ttu-id="fbd31-119">Nome del gruppo risorse ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="fbd31-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="fbd31-120">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="fbd31-120">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="fbd31-121">Opzione Ignora nomi host personalizzati</span><span class="sxs-lookup"><span data-stu-id="fbd31-121">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="fbd31-122">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="fbd31-122">-IgnoreSourceControl</span></span>
<span data-ttu-id="fbd31-123">Opzione Ignora controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="fbd31-123">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="fbd31-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="fbd31-124">-Name</span></span>
<span data-ttu-id="fbd31-125">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="fbd31-125">Webapp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbd31-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbd31-126">-ResourceGroupName</span></span>
<span data-ttu-id="fbd31-127">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="fbd31-127">Resource Group Name</span></span>

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

### <span data-ttu-id="fbd31-128">-Slot</span><span class="sxs-lookup"><span data-stu-id="fbd31-128">-Slot</span></span>
<span data-ttu-id="fbd31-129">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="fbd31-129">Webapp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd31-130">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="fbd31-130">-SourceWebApp</span></span>
<span data-ttu-id="fbd31-131">Oggetto Web App di origine</span><span class="sxs-lookup"><span data-stu-id="fbd31-131">Source WebApp Object</span></span>

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

### <span data-ttu-id="fbd31-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbd31-132">-DefaultProfile</span></span>
<span data-ttu-id="fbd31-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fbd31-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbd31-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbd31-134">CommonParameters</span></span>
<span data-ttu-id="fbd31-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbd31-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbd31-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbd31-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbd31-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fbd31-137">INPUTS</span></span>

### <span data-ttu-id="fbd31-138">Sito</span><span class="sxs-lookup"><span data-stu-id="fbd31-138">Site</span></span>
<span data-ttu-id="fbd31-139">Il parametro "SourceWebApp" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="fbd31-139">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="fbd31-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fbd31-140">OUTPUTS</span></span>

## <span data-ttu-id="fbd31-141">Note</span><span class="sxs-lookup"><span data-stu-id="fbd31-141">NOTES</span></span>

## <span data-ttu-id="fbd31-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fbd31-142">RELATED LINKS</span></span>

[<span data-ttu-id="fbd31-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fbd31-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="fbd31-144">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fbd31-144">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="fbd31-145">Riavviare-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fbd31-145">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="fbd31-146">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fbd31-146">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="fbd31-147">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fbd31-147">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="fbd31-148">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fbd31-148">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="fbd31-149">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fbd31-149">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="fbd31-150">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fbd31-150">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
