---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: 918f590258e6678a66262a6ad2d72a352bf13fd3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676298"
---
# <span data-ttu-id="e2893-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e2893-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="e2893-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2893-102">SYNOPSIS</span></span>
<span data-ttu-id="e2893-103">Crea un piano di servizio app Azure in una determinata posizione geo.</span><span class="sxs-lookup"><span data-stu-id="e2893-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="e2893-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2893-104">SYNTAX</span></span>

### <span data-ttu-id="e2893-105">S1</span><span class="sxs-lookup"><span data-stu-id="e2893-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2893-106">S2</span><span class="sxs-lookup"><span data-stu-id="e2893-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2893-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2893-107">DESCRIPTION</span></span>
<span data-ttu-id="e2893-108">Il cmdlet **New-AzAppServicePlan** crea un piano di servizio app Azure in una determinata posizione geo con il livello specificato, le dimensioni dei lavoratori e il numero di dipendenti.</span><span class="sxs-lookup"><span data-stu-id="e2893-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="e2893-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2893-109">EXAMPLES</span></span>

### <span data-ttu-id="e2893-110">Esempio 1: creare un piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="e2893-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="e2893-111">Questo comando crea un piano di servizio app denominato ContosoASP nel gruppo risorse denominato Default-Web-Westus in Geo location West US.</span><span class="sxs-lookup"><span data-stu-id="e2893-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="e2893-112">Il comando specifica un livello di base e assegna due piccoli lavoratori.</span><span class="sxs-lookup"><span data-stu-id="e2893-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="e2893-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2893-113">PARAMETERS</span></span>

### <span data-ttu-id="e2893-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e2893-114">-AppServicePlan</span></span>
<span data-ttu-id="e2893-115">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="e2893-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="e2893-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="e2893-116">-AseName</span></span>
<span data-ttu-id="e2893-117">Nome ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="e2893-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="e2893-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2893-118">-AseResourceGroupName</span></span>
<span data-ttu-id="e2893-119">Nome del gruppo risorse ambiente servizio app</span><span class="sxs-lookup"><span data-stu-id="e2893-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="e2893-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2893-120">-AsJob</span></span>
<span data-ttu-id="e2893-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e2893-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2893-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2893-122">-DefaultProfile</span></span>
<span data-ttu-id="e2893-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e2893-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2893-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="e2893-124">-HyperV</span></span>
<span data-ttu-id="e2893-125">Specifica questo, il piano di servizio app eseguirà i contenitori Windows</span><span class="sxs-lookup"><span data-stu-id="e2893-125">Specify this, App Service Plan will run Windows Containers</span></span>

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

### <span data-ttu-id="e2893-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e2893-126">-Location</span></span>
<span data-ttu-id="e2893-127">Posizione</span><span class="sxs-lookup"><span data-stu-id="e2893-127">Location</span></span> 

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

### <span data-ttu-id="e2893-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2893-128">-Name</span></span>
<span data-ttu-id="e2893-129">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="e2893-129">App Service Plan Name</span></span>

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

### <span data-ttu-id="e2893-130">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="e2893-130">-NumberofWorkers</span></span>
<span data-ttu-id="e2893-131">Numero di dipendenti</span><span class="sxs-lookup"><span data-stu-id="e2893-131">Number Of Workers</span></span>

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

### <span data-ttu-id="e2893-132">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="e2893-132">-PerSiteScaling</span></span>
<span data-ttu-id="e2893-133">Se abilitare o meno l'attivazione per scala per sito</span><span class="sxs-lookup"><span data-stu-id="e2893-133">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="e2893-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2893-134">-ResourceGroupName</span></span>
<span data-ttu-id="e2893-135">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="e2893-135">Resource Group Name</span></span>

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

### <span data-ttu-id="e2893-136">-Tier</span><span class="sxs-lookup"><span data-stu-id="e2893-136">-Tier</span></span>
<span data-ttu-id="e2893-137">Livello</span><span class="sxs-lookup"><span data-stu-id="e2893-137">Tier</span></span>

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

### <span data-ttu-id="e2893-138">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="e2893-138">-WorkerSize</span></span>
<span data-ttu-id="e2893-139">Dimensioni del Web Worker</span><span class="sxs-lookup"><span data-stu-id="e2893-139">Size of web worker</span></span>

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

### <span data-ttu-id="e2893-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2893-140">CommonParameters</span></span>
<span data-ttu-id="e2893-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2893-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2893-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2893-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2893-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2893-143">INPUTS</span></span>

### <span data-ttu-id="e2893-144">Microsoft. Azure. Commands. webapps. Models. Web App. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e2893-144">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="e2893-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2893-145">OUTPUTS</span></span>

### <span data-ttu-id="e2893-146">Microsoft. Azure. Commands. webapps. Models. Web App. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e2893-146">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="e2893-147">Note</span><span class="sxs-lookup"><span data-stu-id="e2893-147">NOTES</span></span>

## <span data-ttu-id="e2893-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2893-148">RELATED LINKS</span></span>

[<span data-ttu-id="e2893-149">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e2893-149">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="e2893-150">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e2893-150">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="e2893-151">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e2893-151">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)

