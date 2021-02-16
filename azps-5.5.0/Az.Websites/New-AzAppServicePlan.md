---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: 863a1b42a6decd6b979516d21c007a9626e36d23
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207467"
---
# <span data-ttu-id="93402-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="93402-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="93402-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93402-102">SYNOPSIS</span></span>
<span data-ttu-id="93402-103">Crea un piano di servizio app di Azure in una determinata posizione geografica.</span><span class="sxs-lookup"><span data-stu-id="93402-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="93402-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93402-104">SYNTAX</span></span>

### <span data-ttu-id="93402-105">S1</span><span class="sxs-lookup"><span data-stu-id="93402-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-Tag <Hashtable>] [-Linux] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93402-106">S2</span><span class="sxs-lookup"><span data-stu-id="93402-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93402-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="93402-107">DESCRIPTION</span></span>
<span data-ttu-id="93402-108">Il cmdlet **New-AzAppServicePlan** crea un piano di servizio app di Azure in una determinata posizione geografica con il livello, le dimensioni dei dipendenti e il numero di lavoratori specificati.</span><span class="sxs-lookup"><span data-stu-id="93402-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="93402-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93402-109">EXAMPLES</span></span>

### <span data-ttu-id="93402-110">Esempio 1: Creare un piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="93402-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="93402-111">Questo comando crea un piano di servizio app denominato ContosoASP nel gruppo di risorse Default-Web-WestUS in Geo location West US.</span><span class="sxs-lookup"><span data-stu-id="93402-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="93402-112">Il comando specifica un Livello base e assegna due lavoratori di piccole dimensioni.</span><span class="sxs-lookup"><span data-stu-id="93402-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="93402-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93402-113">PARAMETERS</span></span>

### <span data-ttu-id="93402-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="93402-114">-AppServicePlan</span></span>
<span data-ttu-id="93402-115">Oggetto Piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="93402-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="93402-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="93402-116">-AseName</span></span>
<span data-ttu-id="93402-117">Nome dell'ambiente del servizio app</span><span class="sxs-lookup"><span data-stu-id="93402-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="93402-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93402-118">-AseResourceGroupName</span></span>
<span data-ttu-id="93402-119">Nome del gruppo di risorse dell'ambiente del servizio app</span><span class="sxs-lookup"><span data-stu-id="93402-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="93402-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93402-120">-AsJob</span></span>
<span data-ttu-id="93402-121">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="93402-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93402-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93402-122">-DefaultProfile</span></span>
<span data-ttu-id="93402-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93402-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93402-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="93402-124">-HyperV</span></span>
<span data-ttu-id="93402-125">Specificare questo valore, il piano di servizio per le app eseguirà Windows Containers</span><span class="sxs-lookup"><span data-stu-id="93402-125">Specify this, App Service Plan will run Windows Containers</span></span>

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

### <span data-ttu-id="93402-126">-Linux</span><span class="sxs-lookup"><span data-stu-id="93402-126">-Linux</span></span>
<span data-ttu-id="93402-127">Specifica questa opzione, il piano di servizio dell'app eseguirà Linux Containers</span><span class="sxs-lookup"><span data-stu-id="93402-127">Specify this, App Service Plan will run Linux Containers</span></span>

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

### <span data-ttu-id="93402-128">-Location</span><span class="sxs-lookup"><span data-stu-id="93402-128">-Location</span></span>
<span data-ttu-id="93402-129">Posizione</span><span class="sxs-lookup"><span data-stu-id="93402-129">Location</span></span> 

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

### <span data-ttu-id="93402-130">-Name</span><span class="sxs-lookup"><span data-stu-id="93402-130">-Name</span></span>
<span data-ttu-id="93402-131">Nome del piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="93402-131">App Service Plan Name</span></span>

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

### <span data-ttu-id="93402-132">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="93402-132">-NumberofWorkers</span></span>
<span data-ttu-id="93402-133">Numero di dipendenti</span><span class="sxs-lookup"><span data-stu-id="93402-133">Number Of Workers</span></span>

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

### <span data-ttu-id="93402-134">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="93402-134">-PerSiteScaling</span></span>
<span data-ttu-id="93402-135">Attivazione o meno della scalabilità per sito</span><span class="sxs-lookup"><span data-stu-id="93402-135">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="93402-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93402-136">-ResourceGroupName</span></span>
<span data-ttu-id="93402-137">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="93402-137">Resource Group Name</span></span>

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

### <span data-ttu-id="93402-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="93402-138">-Tag</span></span>
<span data-ttu-id="93402-139">I tag sono coppie nome/valore che consentono di categorizzare le risorse</span><span class="sxs-lookup"><span data-stu-id="93402-139">Tags are name/value pairs that enable you to categorize resources</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93402-140">-Livello</span><span class="sxs-lookup"><span data-stu-id="93402-140">-Tier</span></span>
<span data-ttu-id="93402-141">Livello</span><span class="sxs-lookup"><span data-stu-id="93402-141">Tier</span></span>

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

### <span data-ttu-id="93402-142">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="93402-142">-WorkerSize</span></span>
<span data-ttu-id="93402-143">Dimensioni di Web worker</span><span class="sxs-lookup"><span data-stu-id="93402-143">Size of web worker</span></span>

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

### <span data-ttu-id="93402-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93402-144">CommonParameters</span></span>
<span data-ttu-id="93402-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93402-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93402-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="93402-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93402-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="93402-147">INPUTS</span></span>

### <span data-ttu-id="93402-148">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="93402-148">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="93402-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93402-149">OUTPUTS</span></span>

### <span data-ttu-id="93402-150">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="93402-150">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="93402-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="93402-151">NOTES</span></span>

## <span data-ttu-id="93402-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93402-152">RELATED LINKS</span></span>

[<span data-ttu-id="93402-153">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="93402-153">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="93402-154">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="93402-154">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="93402-155">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="93402-155">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


