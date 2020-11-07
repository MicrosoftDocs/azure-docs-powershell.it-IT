---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
ms.openlocfilehash: e03e7dee6e233934216c04a44c1e100d3e26347b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687963"
---
# <span data-ttu-id="67350-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="67350-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="67350-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67350-102">SYNOPSIS</span></span>
<span data-ttu-id="67350-103">Crea un piano di servizio app Azure in una determinata posizione geo.</span><span class="sxs-lookup"><span data-stu-id="67350-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67350-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67350-104">SYNTAX</span></span>

### <span data-ttu-id="67350-105">S1</span><span class="sxs-lookup"><span data-stu-id="67350-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67350-106">S2</span><span class="sxs-lookup"><span data-stu-id="67350-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67350-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67350-107">DESCRIPTION</span></span>
<span data-ttu-id="67350-108">Il cmdlet **New-AzureRmAppServicePlan** crea un piano di servizio app Azure in una determinata posizione geo con il livello specificato, le dimensioni dei lavoratori e il numero di dipendenti.</span><span class="sxs-lookup"><span data-stu-id="67350-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="67350-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67350-109">EXAMPLES</span></span>

### <span data-ttu-id="67350-110">Esempio 1: creare un piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="67350-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="67350-111">Questo comando crea un piano di servizio app denominato ContosoASP nel gruppo risorse denominato Default-Web-Westus in Geo location West US.</span><span class="sxs-lookup"><span data-stu-id="67350-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="67350-112">Il comando specifica un livello di base e assegna due piccoli lavoratori.</span><span class="sxs-lookup"><span data-stu-id="67350-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="67350-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67350-113">PARAMETERS</span></span>

### <span data-ttu-id="67350-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="67350-114">-AppServicePlan</span></span>
<span data-ttu-id="67350-115">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="67350-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="67350-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="67350-116">-AseName</span></span>
<span data-ttu-id="67350-117">Nome ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="67350-117">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67350-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67350-118">-AseResourceGroupName</span></span>
<span data-ttu-id="67350-119">Nome del gruppo risorse ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="67350-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67350-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="67350-120">-Location</span></span>
<span data-ttu-id="67350-121">Posizione</span><span class="sxs-lookup"><span data-stu-id="67350-121">Location</span></span> 

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

### <span data-ttu-id="67350-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="67350-122">-Name</span></span>
<span data-ttu-id="67350-123">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="67350-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="67350-124">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="67350-124">-NumberofWorkers</span></span>
<span data-ttu-id="67350-125">Numero di dipendenti</span><span class="sxs-lookup"><span data-stu-id="67350-125">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67350-126">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="67350-126">-PerSiteScaling</span></span>
<span data-ttu-id="67350-127">Se abilitare o meno l'attivazione per scala per sito</span><span class="sxs-lookup"><span data-stu-id="67350-127">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67350-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67350-128">-ResourceGroupName</span></span>
<span data-ttu-id="67350-129">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="67350-129">Resource Group Name</span></span>

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

### <span data-ttu-id="67350-130">-Tier</span><span class="sxs-lookup"><span data-stu-id="67350-130">-Tier</span></span>
<span data-ttu-id="67350-131">Livello</span><span class="sxs-lookup"><span data-stu-id="67350-131">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67350-132">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="67350-132">-WorkerSize</span></span>
<span data-ttu-id="67350-133">Dimensioni del Web Worker</span><span class="sxs-lookup"><span data-stu-id="67350-133">Size of web worker</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67350-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67350-134">-DefaultProfile</span></span>
<span data-ttu-id="67350-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67350-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67350-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67350-136">CommonParameters</span></span>
<span data-ttu-id="67350-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67350-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67350-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67350-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67350-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67350-139">INPUTS</span></span>

### <span data-ttu-id="67350-140">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="67350-140">ServerFarmWithRichSku</span></span>
<span data-ttu-id="67350-141">Il parametro ' AppServicePlan ' accetta il valore di tipo ' ServerFarmWithRichSku ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="67350-141">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="67350-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67350-142">OUTPUTS</span></span>

### <span data-ttu-id="67350-143">Microsoft. Azure. Management. website. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="67350-143">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="67350-144">Note</span><span class="sxs-lookup"><span data-stu-id="67350-144">NOTES</span></span>

## <span data-ttu-id="67350-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67350-145">RELATED LINKS</span></span>

[<span data-ttu-id="67350-146">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="67350-146">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="67350-147">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="67350-147">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="67350-148">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="67350-148">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


