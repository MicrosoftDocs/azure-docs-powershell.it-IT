---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/powershell/module/az.windowsiotservices/get-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 51e828245c62ddfcbaa925b3a22a916fd9148ada
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010926"
---
# <span data-ttu-id="9c4d9-101">Get-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="9c4d9-101">Get-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="9c4d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c4d9-102">SYNOPSIS</span></span>
<span data-ttu-id="9c4d9-103">Ottenere i metadati non correlati alla sicurezza di un servizio di dispositivi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="9c4d9-103">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="9c4d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c4d9-104">SYNTAX</span></span>

### <span data-ttu-id="9c4d9-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9c4d9-105">List1 (Default)</span></span>
```
Get-AzWindowsIotServicesDevice [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9c4d9-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="9c4d9-106">Get</span></span>
```
Get-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9c4d9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9c4d9-107">GetViaIdentity</span></span>
```
Get-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c4d9-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="9c4d9-108">List</span></span>
```
Get-AzWindowsIotServicesDevice -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9c4d9-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9c4d9-109">DESCRIPTION</span></span>
<span data-ttu-id="9c4d9-110">Ottenere i metadati non correlati alla sicurezza di un servizio di dispositivi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="9c4d9-110">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="9c4d9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c4d9-111">EXAMPLES</span></span>

### <span data-ttu-id="9c4d9-112">Esempio 1: Ottenere tutti i servizi Windows IoT in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="9c4d9-112">Example 1: Get all Windows IoT services under a subscription</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="9c4d9-113">Questo comando recupera tutti i servizi Windows IoT in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="9c4d9-113">This command gets all Windows IoT services under a subscription.</span></span>

### <span data-ttu-id="9c4d9-114">Esempio 2: Ottenere tutti i servizi IoT di Windows in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9c4d9-114">Example 2: Get all Windows IoT services under a resource group</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="9c4d9-115">Questo comando recupera tutti i servizi IoT di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9c4d9-115">This command gets all Windows IoT services under a resource group.</span></span>

### <span data-ttu-id="9c4d9-116">Esempio 3: Ottenere un servizio Windows IoT in base al nome</span><span class="sxs-lookup"><span data-stu-id="9c4d9-116">Example 3: Get a Windows IoT service by name</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="9c4d9-117">Questo comando ottiene un servizio Windows IoT in base al nome.</span><span class="sxs-lookup"><span data-stu-id="9c4d9-117">This command gets a Windows IoT service by name.</span></span>

### <span data-ttu-id="9c4d9-118">Esempio 4: Ottenere un servizio IoT di Windows in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="9c4d9-118">Example 4: Get a Windows IoT service by object</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'
PS C:\> Get-AzWindowsIotServicesDevice -InputObject $wsi

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="9c4d9-119">Questo comando ottiene un servizio Windows IoT in base all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9c4d9-119">This command gets a Windows IoT service by object.</span></span>

### <span data-ttu-id="9c4d9-120">Esempio 4: Ottenere un servizio IoT di Windows tramite pipeline</span><span class="sxs-lookup"><span data-stu-id="9c4d9-120">Example 4: Get a Windows IoT service by pipeline</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com' | Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="9c4d9-121">Questo comando ottiene un servizio IoT di Windows tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="9c4d9-121">This command gets a Windows IoT service by pipeline.</span></span>

## <span data-ttu-id="9c4d9-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c4d9-122">PARAMETERS</span></span>

### <span data-ttu-id="9c4d9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c4d9-123">-DefaultProfile</span></span>
<span data-ttu-id="9c4d9-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c4d9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c4d9-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c4d9-125">-InputObject</span></span>
<span data-ttu-id="9c4d9-126">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="9c4d9-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c4d9-127">-Name</span><span class="sxs-lookup"><span data-stu-id="9c4d9-127">-Name</span></span>
<span data-ttu-id="9c4d9-128">Nome del servizio di dispositivi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="9c4d9-128">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c4d9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c4d9-129">-ResourceGroupName</span></span>
<span data-ttu-id="9c4d9-130">Nome del gruppo di risorse che contiene il servizio di dispositivi IoT di Windows.</span><span class="sxs-lookup"><span data-stu-id="9c4d9-130">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c4d9-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c4d9-131">-SubscriptionId</span></span>
<span data-ttu-id="9c4d9-132">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="9c4d9-132">The subscription identifier.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c4d9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c4d9-133">CommonParameters</span></span>
<span data-ttu-id="9c4d9-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c4d9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c4d9-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9c4d9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c4d9-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="9c4d9-136">INPUTS</span></span>

### <span data-ttu-id="9c4d9-137">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="9c4d9-137">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="9c4d9-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c4d9-138">OUTPUTS</span></span>

### <span data-ttu-id="9c4d9-139">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="9c4d9-139">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="9c4d9-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="9c4d9-140">NOTES</span></span>

<span data-ttu-id="9c4d9-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9c4d9-141">ALIASES</span></span>

<span data-ttu-id="9c4d9-142">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="9c4d9-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9c4d9-143">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="9c4d9-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9c4d9-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9c4d9-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9c4d9-145">INPUTOBJECT <IWindowsIotServicesIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="9c4d9-145">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9c4d9-146">`[DeviceName <String>]`: nome del servizio dispositivi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="9c4d9-146">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="9c4d9-147">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="9c4d9-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9c4d9-148">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il servizio dispositivi IoT di Windows.</span><span class="sxs-lookup"><span data-stu-id="9c4d9-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="9c4d9-149">`[SubscriptionId <String>]`: l'identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="9c4d9-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="9c4d9-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c4d9-150">RELATED LINKS</span></span>

