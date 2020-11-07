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
ms.locfileid: "93676257"
---
# <span data-ttu-id="1abd0-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1abd0-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="1abd0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1abd0-102">SYNOPSIS</span></span>
<span data-ttu-id="1abd0-103">Imposta un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="1abd0-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="1abd0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1abd0-104">SYNTAX</span></span>

### <span data-ttu-id="1abd0-105">S1</span><span class="sxs-lookup"><span data-stu-id="1abd0-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1abd0-106">S2</span><span class="sxs-lookup"><span data-stu-id="1abd0-106">S2</span></span>
```
Set-AzAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1abd0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1abd0-107">DESCRIPTION</span></span>
<span data-ttu-id="1abd0-108">Il cmdlet **set-AzAppServicePlan** imposta un piano di servizio app Azure.</span><span class="sxs-lookup"><span data-stu-id="1abd0-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="1abd0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1abd0-109">EXAMPLES</span></span>

### <span data-ttu-id="1abd0-110">1: modificare un piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="1abd0-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="1abd0-111">Questo comando imposta l'opzione PerSiteScaling su true nel piano di servizio app denominato ContosoASP che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="1abd0-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="1abd0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1abd0-112">PARAMETERS</span></span>

### <span data-ttu-id="1abd0-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="1abd0-113">-AdminSiteName</span></span>
<span data-ttu-id="1abd0-114">Nome sito amministratore</span><span class="sxs-lookup"><span data-stu-id="1abd0-114">Admin Site Name</span></span>

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

### <span data-ttu-id="1abd0-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1abd0-115">-AppServicePlan</span></span>
<span data-ttu-id="1abd0-116">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="1abd0-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="1abd0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1abd0-117">-AsJob</span></span>
<span data-ttu-id="1abd0-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1abd0-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1abd0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1abd0-119">-DefaultProfile</span></span>
<span data-ttu-id="1abd0-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1abd0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1abd0-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1abd0-121">-Name</span></span>
<span data-ttu-id="1abd0-122">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="1abd0-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="1abd0-123">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="1abd0-123">-NumberofWorkers</span></span>
<span data-ttu-id="1abd0-124">Numero di dipendenti</span><span class="sxs-lookup"><span data-stu-id="1abd0-124">Number Of Workers</span></span>

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

### <span data-ttu-id="1abd0-125">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="1abd0-125">-PerSiteScaling</span></span>
<span data-ttu-id="1abd0-126">Booleano scala per sito</span><span class="sxs-lookup"><span data-stu-id="1abd0-126">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="1abd0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1abd0-127">-ResourceGroupName</span></span>
<span data-ttu-id="1abd0-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="1abd0-128">Resource Group Name</span></span>

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

### <span data-ttu-id="1abd0-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="1abd0-129">-Tier</span></span>
<span data-ttu-id="1abd0-130">Livello</span><span class="sxs-lookup"><span data-stu-id="1abd0-130">Tier</span></span>

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

### <span data-ttu-id="1abd0-131">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="1abd0-131">-WorkerSize</span></span>
<span data-ttu-id="1abd0-132">Dimensioni lavoratore</span><span class="sxs-lookup"><span data-stu-id="1abd0-132">Worker Size</span></span>

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

### <span data-ttu-id="1abd0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1abd0-133">CommonParameters</span></span>
<span data-ttu-id="1abd0-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1abd0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1abd0-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1abd0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1abd0-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1abd0-136">INPUTS</span></span>

### <span data-ttu-id="1abd0-137">Microsoft. Azure. Commands. webapps. Models. Web App. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1abd0-137">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="1abd0-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1abd0-138">OUTPUTS</span></span>

### <span data-ttu-id="1abd0-139">Microsoft. Azure. Commands. webapps. Models. Web App. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1abd0-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="1abd0-140">Note</span><span class="sxs-lookup"><span data-stu-id="1abd0-140">NOTES</span></span>

## <span data-ttu-id="1abd0-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1abd0-141">RELATED LINKS</span></span>

[<span data-ttu-id="1abd0-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1abd0-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="1abd0-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1abd0-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="1abd0-144">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1abd0-144">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="1abd0-145">Riavviare-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1abd0-145">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="1abd0-146">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1abd0-146">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="1abd0-147">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1abd0-147">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

