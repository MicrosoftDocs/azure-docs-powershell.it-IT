---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 4b6270a6d56b8f210b2f03311bf19bb09950f361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511208"
---
# <span data-ttu-id="9387b-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9387b-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="9387b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9387b-102">SYNOPSIS</span></span>
<span data-ttu-id="9387b-103">Imposta un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="9387b-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9387b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9387b-104">SYNTAX</span></span>

### <span data-ttu-id="9387b-105">S1</span><span class="sxs-lookup"><span data-stu-id="9387b-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9387b-106">S2</span><span class="sxs-lookup"><span data-stu-id="9387b-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9387b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9387b-107">DESCRIPTION</span></span>
<span data-ttu-id="9387b-108">Il cmdlet **set-AzureRmAppServicePlan** imposta un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="9387b-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="9387b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9387b-109">EXAMPLES</span></span>

### <span data-ttu-id="9387b-110">1: modificare un piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="9387b-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="9387b-111">Questo comando imposta l'opzione PerSiteScaling su true nel piano di servizio app denominato ContosoASP che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="9387b-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="9387b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9387b-112">PARAMETERS</span></span>

### <span data-ttu-id="9387b-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="9387b-113">-AdminSiteName</span></span>
<span data-ttu-id="9387b-114">Nome sito amministratore</span><span class="sxs-lookup"><span data-stu-id="9387b-114">Admin Site Name</span></span>

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

### <span data-ttu-id="9387b-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9387b-115">-AppServicePlan</span></span>
<span data-ttu-id="9387b-116">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="9387b-116">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9387b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="9387b-117">-Name</span></span>
<span data-ttu-id="9387b-118">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="9387b-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="9387b-119">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="9387b-119">-NumberofWorkers</span></span>
<span data-ttu-id="9387b-120">Numero di dipendenti</span><span class="sxs-lookup"><span data-stu-id="9387b-120">Number Of Workers</span></span>

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

### <span data-ttu-id="9387b-121">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="9387b-121">-PerSiteScaling</span></span>
<span data-ttu-id="9387b-122">Booleano scala per sito</span><span class="sxs-lookup"><span data-stu-id="9387b-122">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="9387b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9387b-123">-ResourceGroupName</span></span>
<span data-ttu-id="9387b-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="9387b-124">Resource Group Name</span></span>

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

### <span data-ttu-id="9387b-125">-Tier</span><span class="sxs-lookup"><span data-stu-id="9387b-125">-Tier</span></span>
<span data-ttu-id="9387b-126">Livello</span><span class="sxs-lookup"><span data-stu-id="9387b-126">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9387b-127">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="9387b-127">-WorkerSize</span></span>
<span data-ttu-id="9387b-128">Dimensioni lavoratore</span><span class="sxs-lookup"><span data-stu-id="9387b-128">Worker Size</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9387b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9387b-129">-DefaultProfile</span></span>
<span data-ttu-id="9387b-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9387b-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9387b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9387b-131">CommonParameters</span></span>
<span data-ttu-id="9387b-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9387b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9387b-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9387b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9387b-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9387b-134">INPUTS</span></span>

### <span data-ttu-id="9387b-135">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="9387b-135">ServerFarmWithRichSku</span></span>
<span data-ttu-id="9387b-136">Il parametro ' AppServicePlan ' accetta il valore di tipo ' ServerFarmWithRichSku ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="9387b-136">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="9387b-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9387b-137">OUTPUTS</span></span>

### <span data-ttu-id="9387b-138">Microsoft. Azure. Management. website. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="9387b-138">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="9387b-139">Note</span><span class="sxs-lookup"><span data-stu-id="9387b-139">NOTES</span></span>

## <span data-ttu-id="9387b-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9387b-140">RELATED LINKS</span></span>

[<span data-ttu-id="9387b-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9387b-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="9387b-142">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9387b-142">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="9387b-143">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9387b-143">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="9387b-144">Riavviare-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9387b-144">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="9387b-145">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9387b-145">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="9387b-146">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9387b-146">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


