---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: d27dc8ae315eb587ccb129125500a86e22429773
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858066"
---
# <span data-ttu-id="d9eea-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d9eea-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="d9eea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9eea-102">SYNOPSIS</span></span>
<span data-ttu-id="d9eea-103">Imposta un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="d9eea-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="d9eea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9eea-104">SYNTAX</span></span>

### <span data-ttu-id="d9eea-105">S1</span><span class="sxs-lookup"><span data-stu-id="d9eea-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9eea-106">S2</span><span class="sxs-lookup"><span data-stu-id="d9eea-106">S2</span></span>
```
Set-AzAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9eea-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9eea-107">DESCRIPTION</span></span>
<span data-ttu-id="d9eea-108">Il cmdlet **set-AzAppServicePlan** imposta un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="d9eea-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="d9eea-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9eea-109">EXAMPLES</span></span>

### <span data-ttu-id="d9eea-110">1: modificare un piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="d9eea-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="d9eea-111">Questo comando imposta l'opzione PerSiteScaling su true nel piano di servizio app denominato ContosoASP che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="d9eea-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d9eea-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9eea-112">PARAMETERS</span></span>

### <span data-ttu-id="d9eea-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="d9eea-113">-AdminSiteName</span></span>
<span data-ttu-id="d9eea-114">Nome sito amministratore</span><span class="sxs-lookup"><span data-stu-id="d9eea-114">Admin Site Name</span></span>

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

### <span data-ttu-id="d9eea-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d9eea-115">-AppServicePlan</span></span>
<span data-ttu-id="d9eea-116">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="d9eea-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="d9eea-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9eea-117">-AsJob</span></span>
<span data-ttu-id="d9eea-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d9eea-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9eea-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9eea-119">-DefaultProfile</span></span>
<span data-ttu-id="d9eea-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9eea-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9eea-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9eea-121">-Name</span></span>
<span data-ttu-id="d9eea-122">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="d9eea-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="d9eea-123">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="d9eea-123">-NumberofWorkers</span></span>
<span data-ttu-id="d9eea-124">Numero di dipendenti</span><span class="sxs-lookup"><span data-stu-id="d9eea-124">Number Of Workers</span></span>

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

### <span data-ttu-id="d9eea-125">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="d9eea-125">-PerSiteScaling</span></span>
<span data-ttu-id="d9eea-126">Booleano scala per sito</span><span class="sxs-lookup"><span data-stu-id="d9eea-126">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="d9eea-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9eea-127">-ResourceGroupName</span></span>
<span data-ttu-id="d9eea-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="d9eea-128">Resource Group Name</span></span>

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

### <span data-ttu-id="d9eea-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="d9eea-129">-Tier</span></span>
<span data-ttu-id="d9eea-130">Livello</span><span class="sxs-lookup"><span data-stu-id="d9eea-130">Tier</span></span>

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

### <span data-ttu-id="d9eea-131">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="d9eea-131">-WorkerSize</span></span>
<span data-ttu-id="d9eea-132">Dimensioni lavoratore</span><span class="sxs-lookup"><span data-stu-id="d9eea-132">Worker Size</span></span>

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

### <span data-ttu-id="d9eea-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9eea-133">CommonParameters</span></span>
<span data-ttu-id="d9eea-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9eea-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9eea-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9eea-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9eea-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9eea-136">INPUTS</span></span>

### <span data-ttu-id="d9eea-137">Microsoft. Azure. Commands. webapps. Models. Web App. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d9eea-137">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="d9eea-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9eea-138">OUTPUTS</span></span>

### <span data-ttu-id="d9eea-139">Microsoft. Azure. Commands. webapps. Models. Web App. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d9eea-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="d9eea-140">Note</span><span class="sxs-lookup"><span data-stu-id="d9eea-140">NOTES</span></span>

## <span data-ttu-id="d9eea-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9eea-141">RELATED LINKS</span></span>

[<span data-ttu-id="d9eea-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d9eea-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="d9eea-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d9eea-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="d9eea-144">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d9eea-144">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="d9eea-145">Riavviare-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d9eea-145">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="d9eea-146">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d9eea-146">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="d9eea-147">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d9eea-147">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


