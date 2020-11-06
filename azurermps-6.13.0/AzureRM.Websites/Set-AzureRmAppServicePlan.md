---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 2163c18fecadba069b7c3fba260ab81538ed5583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516296"
---
# <span data-ttu-id="ef255-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ef255-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="ef255-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ef255-102">SYNOPSIS</span></span>
<span data-ttu-id="ef255-103">Imposta un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="ef255-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef255-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef255-104">SYNTAX</span></span>

### <span data-ttu-id="ef255-105">S1</span><span class="sxs-lookup"><span data-stu-id="ef255-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef255-106">S2</span><span class="sxs-lookup"><span data-stu-id="ef255-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef255-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef255-107">DESCRIPTION</span></span>
<span data-ttu-id="ef255-108">Il cmdlet **set-AzureRmAppServicePlan** imposta un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="ef255-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="ef255-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef255-109">EXAMPLES</span></span>

### <span data-ttu-id="ef255-110">1: modificare un piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="ef255-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="ef255-111">Questo comando imposta l'opzione PerSiteScaling su true nel piano di servizio app denominato ContosoASP che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="ef255-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ef255-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ef255-112">PARAMETERS</span></span>

### <span data-ttu-id="ef255-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="ef255-113">-AdminSiteName</span></span>
<span data-ttu-id="ef255-114">Nome sito amministratore</span><span class="sxs-lookup"><span data-stu-id="ef255-114">Admin Site Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef255-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ef255-115">-AppServicePlan</span></span>
<span data-ttu-id="ef255-116">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="ef255-116">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef255-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef255-117">-AsJob</span></span>
<span data-ttu-id="ef255-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ef255-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef255-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef255-119">-DefaultProfile</span></span>
<span data-ttu-id="ef255-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ef255-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef255-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef255-121">-Name</span></span>
<span data-ttu-id="ef255-122">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="ef255-122">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef255-123">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="ef255-123">-NumberofWorkers</span></span>
<span data-ttu-id="ef255-124">Numero di dipendenti</span><span class="sxs-lookup"><span data-stu-id="ef255-124">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: S1
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef255-125">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="ef255-125">-PerSiteScaling</span></span>
<span data-ttu-id="ef255-126">Booleano scala per sito</span><span class="sxs-lookup"><span data-stu-id="ef255-126">Per Site Scaling Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef255-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef255-127">-ResourceGroupName</span></span>
<span data-ttu-id="ef255-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ef255-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef255-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="ef255-129">-Tier</span></span>
<span data-ttu-id="ef255-130">Livello</span><span class="sxs-lookup"><span data-stu-id="ef255-130">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef255-131">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="ef255-131">-WorkerSize</span></span>
<span data-ttu-id="ef255-132">Dimensioni lavoratore</span><span class="sxs-lookup"><span data-stu-id="ef255-132">Worker Size</span></span>

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

### <span data-ttu-id="ef255-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef255-133">CommonParameters</span></span>
<span data-ttu-id="ef255-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef255-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef255-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef255-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef255-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ef255-136">INPUTS</span></span>

### <span data-ttu-id="ef255-137">Microsoft. Azure. Management. website. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ef255-137">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="ef255-138">Parametri: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ef255-138">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="ef255-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef255-139">OUTPUTS</span></span>

### <span data-ttu-id="ef255-140">Microsoft. Azure. Management. website. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ef255-140">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>

## <span data-ttu-id="ef255-141">Note</span><span class="sxs-lookup"><span data-stu-id="ef255-141">NOTES</span></span>

## <span data-ttu-id="ef255-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef255-142">RELATED LINKS</span></span>

[<span data-ttu-id="ef255-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ef255-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="ef255-144">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ef255-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="ef255-145">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ef255-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="ef255-146">Riavviare-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ef255-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="ef255-147">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ef255-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="ef255-148">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ef255-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


