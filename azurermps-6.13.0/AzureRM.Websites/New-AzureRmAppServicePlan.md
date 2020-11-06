---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
ms.openlocfilehash: 09300c7d7d8394dbcfed36560c988f0193473c24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507252"
---
# <span data-ttu-id="b8f04-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b8f04-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="b8f04-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b8f04-102">SYNOPSIS</span></span>
<span data-ttu-id="b8f04-103">Crea un piano di servizio app Azure in una determinata posizione geo.</span><span class="sxs-lookup"><span data-stu-id="b8f04-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8f04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b8f04-104">SYNTAX</span></span>

### <span data-ttu-id="b8f04-105">S1</span><span class="sxs-lookup"><span data-stu-id="b8f04-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8f04-106">S2</span><span class="sxs-lookup"><span data-stu-id="b8f04-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8f04-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8f04-107">DESCRIPTION</span></span>
<span data-ttu-id="b8f04-108">Il cmdlet **New-AzureRmAppServicePlan** crea un piano di servizio app Azure in una determinata posizione geo con il livello specificato, le dimensioni dei lavoratori e il numero di dipendenti.</span><span class="sxs-lookup"><span data-stu-id="b8f04-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="b8f04-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b8f04-109">EXAMPLES</span></span>

### <span data-ttu-id="b8f04-110">Esempio 1: creare un piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="b8f04-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="b8f04-111">Questo comando crea un piano di servizio app denominato ContosoASP nel gruppo risorse denominato Default-Web-Westus in Geo location West US.</span><span class="sxs-lookup"><span data-stu-id="b8f04-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="b8f04-112">Il comando specifica un livello di base e assegna due piccoli lavoratori.</span><span class="sxs-lookup"><span data-stu-id="b8f04-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="b8f04-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b8f04-113">PARAMETERS</span></span>

### <span data-ttu-id="b8f04-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b8f04-114">-AppServicePlan</span></span>
<span data-ttu-id="b8f04-115">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="b8f04-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="b8f04-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="b8f04-116">-AseName</span></span>
<span data-ttu-id="b8f04-117">Nome ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="b8f04-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="b8f04-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8f04-118">-AseResourceGroupName</span></span>
<span data-ttu-id="b8f04-119">Nome del gruppo risorse ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="b8f04-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="b8f04-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8f04-120">-AsJob</span></span>
<span data-ttu-id="b8f04-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b8f04-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8f04-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8f04-122">-DefaultProfile</span></span>
<span data-ttu-id="b8f04-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b8f04-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8f04-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="b8f04-124">-HyperV</span></span>
<span data-ttu-id="b8f04-125">Specifica questo, il piano di servizio app eseguirà i contenitori Windows</span><span class="sxs-lookup"><span data-stu-id="b8f04-125">Specify this, App Service Plan will run Windows Containers</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8f04-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b8f04-126">-Location</span></span>
<span data-ttu-id="b8f04-127">Posizione</span><span class="sxs-lookup"><span data-stu-id="b8f04-127">Location</span></span> 

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

### <span data-ttu-id="b8f04-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8f04-128">-Name</span></span>
<span data-ttu-id="b8f04-129">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="b8f04-129">App Service Plan Name</span></span>

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

### <span data-ttu-id="b8f04-130">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="b8f04-130">-NumberofWorkers</span></span>
<span data-ttu-id="b8f04-131">Numero di dipendenti</span><span class="sxs-lookup"><span data-stu-id="b8f04-131">Number Of Workers</span></span>

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

### <span data-ttu-id="b8f04-132">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="b8f04-132">-PerSiteScaling</span></span>
<span data-ttu-id="b8f04-133">Se abilitare o meno l'attivazione per scala per sito</span><span class="sxs-lookup"><span data-stu-id="b8f04-133">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="b8f04-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8f04-134">-ResourceGroupName</span></span>
<span data-ttu-id="b8f04-135">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b8f04-135">Resource Group Name</span></span>

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

### <span data-ttu-id="b8f04-136">-Tier</span><span class="sxs-lookup"><span data-stu-id="b8f04-136">-Tier</span></span>
<span data-ttu-id="b8f04-137">Livello</span><span class="sxs-lookup"><span data-stu-id="b8f04-137">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8f04-138">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="b8f04-138">-WorkerSize</span></span>
<span data-ttu-id="b8f04-139">Dimensioni del Web Worker</span><span class="sxs-lookup"><span data-stu-id="b8f04-139">Size of web worker</span></span>

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

### <span data-ttu-id="b8f04-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8f04-140">CommonParameters</span></span>
<span data-ttu-id="b8f04-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8f04-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8f04-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8f04-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8f04-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b8f04-143">INPUTS</span></span>

### <span data-ttu-id="b8f04-144">Microsoft. Azure. Management. website. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b8f04-144">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="b8f04-145">Parametri: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b8f04-145">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="b8f04-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b8f04-146">OUTPUTS</span></span>

### <span data-ttu-id="b8f04-147">Microsoft. Azure. Management. website. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b8f04-147">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>

## <span data-ttu-id="b8f04-148">Note</span><span class="sxs-lookup"><span data-stu-id="b8f04-148">NOTES</span></span>

## <span data-ttu-id="b8f04-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b8f04-149">RELATED LINKS</span></span>

[<span data-ttu-id="b8f04-150">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b8f04-150">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="b8f04-151">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b8f04-151">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="b8f04-152">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b8f04-152">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


