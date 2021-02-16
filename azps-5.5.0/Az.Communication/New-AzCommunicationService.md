---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/new-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
ms.openlocfilehash: 821590b158478c38e5d4e997254e98a802d4befd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199382"
---
# <span data-ttu-id="f3451-101">New-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="f3451-101">New-AzCommunicationService</span></span>

## <span data-ttu-id="f3451-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3451-102">SYNOPSIS</span></span>
<span data-ttu-id="f3451-103">Creare un nuovo servizio di comunicazione o aggiornare un servizio di comunicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="f3451-103">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="f3451-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3451-104">SYNTAX</span></span>

```
New-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DataLocation <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f3451-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f3451-105">DESCRIPTION</span></span>
<span data-ttu-id="f3451-106">Creare un nuovo servizio di comunicazione o aggiornare un servizio di comunicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="f3451-106">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="f3451-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3451-107">EXAMPLES</span></span>

### <span data-ttu-id="f3451-108">Esempio 1: Creare una risorsa ACS</span><span class="sxs-lookup"><span data-stu-id="f3451-108">Example 1: Create a ACS resource</span></span>
```powershell
PS C:\> New-AzCommunicationService -ResourceGroupName ContosoResourceProvider1 -Name ContosoAcsResource1 -DataLocation UnitedStates -Location Global

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="f3451-109">Crea una risorsa ACS usando i parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="f3451-109">Creates a ACS resource using the specified parameters.</span></span>

## <span data-ttu-id="f3451-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3451-110">PARAMETERS</span></span>

### <span data-ttu-id="f3451-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3451-111">-AsJob</span></span>
<span data-ttu-id="f3451-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="f3451-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f3451-113">-DataLocation</span><span class="sxs-lookup"><span data-stu-id="f3451-113">-DataLocation</span></span>
<span data-ttu-id="f3451-114">Posizione in cui il servizio di comunicazione archivia i dati archiviati.</span><span class="sxs-lookup"><span data-stu-id="f3451-114">The location where the communication service stores its data at rest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3451-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3451-115">-DefaultProfile</span></span>
<span data-ttu-id="f3451-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3451-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3451-117">-Location</span><span class="sxs-lookup"><span data-stu-id="f3451-117">-Location</span></span>
<span data-ttu-id="f3451-118">Posizione di Azure in cui è in esecuzione CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="f3451-118">The Azure location where the CommunicationService is running.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3451-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f3451-119">-Name</span></span>
<span data-ttu-id="f3451-120">Nome della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="f3451-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3451-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f3451-121">-NoWait</span></span>
<span data-ttu-id="f3451-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="f3451-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f3451-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3451-123">-ResourceGroupName</span></span>
<span data-ttu-id="f3451-124">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f3451-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f3451-125">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="f3451-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3451-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3451-126">-SubscriptionId</span></span>
<span data-ttu-id="f3451-127">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f3451-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f3451-128">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="f3451-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3451-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="f3451-129">-Tag</span></span>
<span data-ttu-id="f3451-130">Tag del servizio, ovvero un elenco di coppie di valori chiave che descrivono la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f3451-130">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3451-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3451-131">-Confirm</span></span>
<span data-ttu-id="f3451-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3451-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3451-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3451-133">-WhatIf</span></span>
<span data-ttu-id="f3451-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3451-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3451-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3451-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3451-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3451-136">CommonParameters</span></span>
<span data-ttu-id="f3451-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3451-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3451-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f3451-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3451-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="f3451-139">INPUTS</span></span>

## <span data-ttu-id="f3451-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3451-140">OUTPUTS</span></span>

### <span data-ttu-id="f3451-141">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="f3451-141">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="f3451-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="f3451-142">NOTES</span></span>

<span data-ttu-id="f3451-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f3451-143">ALIASES</span></span>

## <span data-ttu-id="f3451-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3451-144">RELATED LINKS</span></span>

