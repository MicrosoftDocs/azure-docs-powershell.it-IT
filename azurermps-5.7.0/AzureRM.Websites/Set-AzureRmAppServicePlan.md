---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 16b2c8df737047619366ebf6b75a4c2ed2264fdc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519803"
---
# <span data-ttu-id="ade4f-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ade4f-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="ade4f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ade4f-102">SYNOPSIS</span></span>
<span data-ttu-id="ade4f-103">Imposta un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="ade4f-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ade4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ade4f-104">SYNTAX</span></span>

### <span data-ttu-id="ade4f-105">S1</span><span class="sxs-lookup"><span data-stu-id="ade4f-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ade4f-106">S2</span><span class="sxs-lookup"><span data-stu-id="ade4f-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ade4f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ade4f-107">DESCRIPTION</span></span>
<span data-ttu-id="ade4f-108">Il cmdlet **set-AzureRmAppServicePlan** imposta un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="ade4f-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="ade4f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ade4f-109">EXAMPLES</span></span>

### <span data-ttu-id="ade4f-110">1: modificare un piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="ade4f-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="ade4f-111">Questo comando imposta l'opzione PerSiteScaling su true nel piano di servizio app denominato ContosoASP che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="ade4f-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ade4f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ade4f-112">PARAMETERS</span></span>

### <span data-ttu-id="ade4f-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="ade4f-113">-AdminSiteName</span></span>
<span data-ttu-id="ade4f-114">Nome sito amministratore</span><span class="sxs-lookup"><span data-stu-id="ade4f-114">Admin Site Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade4f-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ade4f-115">-AppServicePlan</span></span>
<span data-ttu-id="ade4f-116">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="ade4f-116">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ade4f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade4f-117">-DefaultProfile</span></span>
<span data-ttu-id="ade4f-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ade4f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ade4f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ade4f-119">-Name</span></span>
<span data-ttu-id="ade4f-120">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="ade4f-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade4f-121">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="ade4f-121">-NumberofWorkers</span></span>
<span data-ttu-id="ade4f-122">Numero di dipendenti</span><span class="sxs-lookup"><span data-stu-id="ade4f-122">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade4f-123">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="ade4f-123">-PerSiteScaling</span></span>
<span data-ttu-id="ade4f-124">Booleano scala per sito</span><span class="sxs-lookup"><span data-stu-id="ade4f-124">Per Site Scaling Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade4f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ade4f-125">-ResourceGroupName</span></span>
<span data-ttu-id="ade4f-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ade4f-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade4f-127">-Tier</span><span class="sxs-lookup"><span data-stu-id="ade4f-127">-Tier</span></span>
<span data-ttu-id="ade4f-128">Livello</span><span class="sxs-lookup"><span data-stu-id="ade4f-128">Tier</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade4f-129">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="ade4f-129">-WorkerSize</span></span>
<span data-ttu-id="ade4f-130">Dimensioni lavoratore</span><span class="sxs-lookup"><span data-stu-id="ade4f-130">Worker Size</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="ade4f-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ade4f-131">-AsJob</span></span>
<span data-ttu-id="ade4f-132">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ade4f-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ade4f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade4f-133">CommonParameters</span></span>
<span data-ttu-id="ade4f-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ade4f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade4f-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ade4f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade4f-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ade4f-136">INPUTS</span></span>

### <span data-ttu-id="ade4f-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="ade4f-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="ade4f-138">Il parametro ' AppServicePlan ' accetta il valore di tipo ' ServerFarmWithRichSku ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ade4f-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="ade4f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ade4f-139">OUTPUTS</span></span>

### <span data-ttu-id="ade4f-140">Microsoft. Azure. Management. website. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="ade4f-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="ade4f-141">Note</span><span class="sxs-lookup"><span data-stu-id="ade4f-141">NOTES</span></span>

## <span data-ttu-id="ade4f-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ade4f-142">RELATED LINKS</span></span>

[<span data-ttu-id="ade4f-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ade4f-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="ade4f-144">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ade4f-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="ade4f-145">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ade4f-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="ade4f-146">Riavviare-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ade4f-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="ade4f-147">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ade4f-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="ade4f-148">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ade4f-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


