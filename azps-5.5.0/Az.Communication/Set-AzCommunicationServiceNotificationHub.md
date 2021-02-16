---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/set-azcommunicationservicenotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
ms.openlocfilehash: aa9084f067131abb780de798dcd1af0ed8f9d235
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177790"
---
# <span data-ttu-id="650cb-101">Set-AzCommunicationServiceNotificationHub</span><span class="sxs-lookup"><span data-stu-id="650cb-101">Set-AzCommunicationServiceNotificationHub</span></span>

## <span data-ttu-id="650cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="650cb-102">SYNOPSIS</span></span>
<span data-ttu-id="650cb-103">Collega un Hub di notifica di Azure a questo servizio di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="650cb-103">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="650cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="650cb-104">SYNTAX</span></span>

### <span data-ttu-id="650cb-105">LinkExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="650cb-105">LinkExpanded (Default)</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -ConnectionString <String> -NotificationHubResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="650cb-106">Collegamento</span><span class="sxs-lookup"><span data-stu-id="650cb-106">Link</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -LinkNotificationHubParameter <ILinkNotificationHubParameters> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="650cb-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="650cb-107">DESCRIPTION</span></span>
<span data-ttu-id="650cb-108">Collega un Hub di notifica di Azure a questo servizio di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="650cb-108">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="650cb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="650cb-109">EXAMPLES</span></span>

### <span data-ttu-id="650cb-110">Esempio 1: Fornire i dettagli dell'Hub di notifica in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="650cb-110">Example 1: Provide Notification Hub details interactively</span></span>
```powershell
PS C:\> Set-AzCommunicationServiceNotificationHub -CommunicationServiceName ContosoAcsResource2 -ResourceGroupName ContosoResourceProvider1 -ConnectionString "<notificationhub-connectionstring>" -NotificationHubResourceId "<notificationhub-resourceid>"
```

<span data-ttu-id="650cb-111">Un hub di notifica collegato consente a una risorsa ACS di inviare notifiche per determinati eventi.</span><span class="sxs-lookup"><span data-stu-id="650cb-111">A linked notification hub allows a ACS resource to send notifications for certain events.</span></span>

## <span data-ttu-id="650cb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="650cb-112">PARAMETERS</span></span>

### <span data-ttu-id="650cb-113">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="650cb-113">-CommunicationServiceName</span></span>
<span data-ttu-id="650cb-114">Nome della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="650cb-114">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="650cb-115">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="650cb-115">-ConnectionString</span></span>
<span data-ttu-id="650cb-116">Stringa di connessione per l'hub di notifica</span><span class="sxs-lookup"><span data-stu-id="650cb-116">Connection string for the notification hub</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="650cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="650cb-117">-DefaultProfile</span></span>
<span data-ttu-id="650cb-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="650cb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="650cb-119">-LinkNotificationHubParameter</span><span class="sxs-lookup"><span data-stu-id="650cb-119">-LinkNotificationHubParameter</span></span>
<span data-ttu-id="650cb-120">Descrizione di un hub di notifica di Azure da collegare al servizio di comunicazione Da creare, vedere la sezione NOTE per le proprietà LINKNOTIFICATIONHUBPARAMETER e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="650cb-120">Description of an Azure Notification Hub to link to the communication service To construct, see NOTES section for LINKNOTIFICATIONHUBPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters
Parameter Sets: Link
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="650cb-121">-NotificationHubResourceId</span><span class="sxs-lookup"><span data-stu-id="650cb-121">-NotificationHubResourceId</span></span>
<span data-ttu-id="650cb-122">ID risorsa dell'hub di notifica</span><span class="sxs-lookup"><span data-stu-id="650cb-122">The resource ID of the notification hub</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="650cb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="650cb-123">-ResourceGroupName</span></span>
<span data-ttu-id="650cb-124">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="650cb-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="650cb-125">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="650cb-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="650cb-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="650cb-126">-SubscriptionId</span></span>
<span data-ttu-id="650cb-127">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="650cb-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="650cb-128">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="650cb-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="650cb-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="650cb-129">-Confirm</span></span>
<span data-ttu-id="650cb-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="650cb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="650cb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="650cb-131">-WhatIf</span></span>
<span data-ttu-id="650cb-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="650cb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="650cb-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="650cb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="650cb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="650cb-134">CommonParameters</span></span>
<span data-ttu-id="650cb-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="650cb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="650cb-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="650cb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="650cb-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="650cb-137">INPUTS</span></span>

### <span data-ttu-id="650cb-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span><span class="sxs-lookup"><span data-stu-id="650cb-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span></span>

## <span data-ttu-id="650cb-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="650cb-139">OUTPUTS</span></span>

### <span data-ttu-id="650cb-140">System.String</span><span class="sxs-lookup"><span data-stu-id="650cb-140">System.String</span></span>

## <span data-ttu-id="650cb-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="650cb-141">NOTES</span></span>

<span data-ttu-id="650cb-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="650cb-142">ALIASES</span></span>

<span data-ttu-id="650cb-143">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="650cb-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="650cb-144">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="650cb-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="650cb-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="650cb-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="650cb-146">LINKNOTIFICATIONHUBPARAMETER: <ILinkNotificationHubParameters> Descrizione di un hub di notifica di Azure da collegare al servizio di comunicazione</span><span class="sxs-lookup"><span data-stu-id="650cb-146">LINKNOTIFICATIONHUBPARAMETER <ILinkNotificationHubParameters>: Description of an Azure Notification Hub to link to the communication service</span></span>
  - <span data-ttu-id="650cb-147">`ConnectionString <String>`: stringa di connessione per l'hub di notifica</span><span class="sxs-lookup"><span data-stu-id="650cb-147">`ConnectionString <String>`: Connection string for the notification hub</span></span>
  - <span data-ttu-id="650cb-148">`ResourceId <String>`: ID risorsa dell'hub di notifica</span><span class="sxs-lookup"><span data-stu-id="650cb-148">`ResourceId <String>`: The resource ID of the notification hub</span></span>

## <span data-ttu-id="650cb-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="650cb-149">RELATED LINKS</span></span>

