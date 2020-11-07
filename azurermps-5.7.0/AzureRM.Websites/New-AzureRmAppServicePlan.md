---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
ms.openlocfilehash: 09491e82a1eb0ab6b77a382fc727d385bbd6820f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687400"
---
# <span data-ttu-id="3a5b8-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3a5b8-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="3a5b8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a5b8-102">SYNOPSIS</span></span>
<span data-ttu-id="3a5b8-103">Crea un piano di servizio app Azure in una determinata posizione geo.</span><span class="sxs-lookup"><span data-stu-id="3a5b8-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a5b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a5b8-104">SYNTAX</span></span>

### <span data-ttu-id="3a5b8-105">S1</span><span class="sxs-lookup"><span data-stu-id="3a5b8-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob][-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a5b8-106">S2</span><span class="sxs-lookup"><span data-stu-id="3a5b8-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a5b8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a5b8-107">DESCRIPTION</span></span>
<span data-ttu-id="3a5b8-108">Il cmdlet **New-AzureRmAppServicePlan** crea un piano di servizio app Azure in una determinata posizione geo con il livello specificato, le dimensioni dei lavoratori e il numero di dipendenti.</span><span class="sxs-lookup"><span data-stu-id="3a5b8-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="3a5b8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a5b8-109">EXAMPLES</span></span>

### <span data-ttu-id="3a5b8-110">Esempio 1: creare un piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="3a5b8-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="3a5b8-111">Questo comando crea un piano di servizio app denominato ContosoASP nel gruppo risorse denominato Default-Web-Westus in Geo location West US.</span><span class="sxs-lookup"><span data-stu-id="3a5b8-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="3a5b8-112">Il comando specifica un livello di base e assegna due piccoli lavoratori.</span><span class="sxs-lookup"><span data-stu-id="3a5b8-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="3a5b8-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a5b8-113">PARAMETERS</span></span>

### <span data-ttu-id="3a5b8-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3a5b8-114">-AppServicePlan</span></span>
<span data-ttu-id="3a5b8-115">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="3a5b8-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="3a5b8-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="3a5b8-116">-AseName</span></span>
<span data-ttu-id="3a5b8-117">Nome ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="3a5b8-117">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a5b8-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a5b8-118">-AseResourceGroupName</span></span>
<span data-ttu-id="3a5b8-119">Nome del gruppo risorse ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="3a5b8-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a5b8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a5b8-120">-DefaultProfile</span></span>
<span data-ttu-id="3a5b8-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a5b8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a5b8-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3a5b8-122">-Location</span></span>
<span data-ttu-id="3a5b8-123">Posizione</span><span class="sxs-lookup"><span data-stu-id="3a5b8-123">Location</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a5b8-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a5b8-124">-Name</span></span>
<span data-ttu-id="3a5b8-125">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="3a5b8-125">App Service Plan Name</span></span>

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

### <span data-ttu-id="3a5b8-126">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="3a5b8-126">-NumberofWorkers</span></span>
<span data-ttu-id="3a5b8-127">Numero di dipendenti</span><span class="sxs-lookup"><span data-stu-id="3a5b8-127">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a5b8-128">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="3a5b8-128">-PerSiteScaling</span></span>
<span data-ttu-id="3a5b8-129">Se abilitare o meno l'attivazione per scala per sito</span><span class="sxs-lookup"><span data-stu-id="3a5b8-129">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a5b8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a5b8-130">-ResourceGroupName</span></span>
<span data-ttu-id="3a5b8-131">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="3a5b8-131">Resource Group Name</span></span>

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

### <span data-ttu-id="3a5b8-132">-Tier</span><span class="sxs-lookup"><span data-stu-id="3a5b8-132">-Tier</span></span>
<span data-ttu-id="3a5b8-133">Livello</span><span class="sxs-lookup"><span data-stu-id="3a5b8-133">Tier</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a5b8-134">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="3a5b8-134">-WorkerSize</span></span>
<span data-ttu-id="3a5b8-135">Dimensioni del Web Worker</span><span class="sxs-lookup"><span data-stu-id="3a5b8-135">Size of web worker</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="3a5b8-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a5b8-136">-AsJob</span></span>
<span data-ttu-id="3a5b8-137">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3a5b8-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a5b8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a5b8-138">CommonParameters</span></span>
<span data-ttu-id="3a5b8-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a5b8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a5b8-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a5b8-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a5b8-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a5b8-141">INPUTS</span></span>

### <span data-ttu-id="3a5b8-142">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="3a5b8-142">ServerFarmWithRichSku</span></span>
<span data-ttu-id="3a5b8-143">Il parametro ' AppServicePlan ' accetta il valore di tipo ' ServerFarmWithRichSku ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3a5b8-143">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="3a5b8-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a5b8-144">OUTPUTS</span></span>

### <span data-ttu-id="3a5b8-145">Microsoft. Azure. Management. website. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="3a5b8-145">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="3a5b8-146">Note</span><span class="sxs-lookup"><span data-stu-id="3a5b8-146">NOTES</span></span>

## <span data-ttu-id="3a5b8-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a5b8-147">RELATED LINKS</span></span>

[<span data-ttu-id="3a5b8-148">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3a5b8-148">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="3a5b8-149">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3a5b8-149">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="3a5b8-150">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3a5b8-150">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


