---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/get-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
ms.openlocfilehash: b9236dc7c3e4a12c9be6b72cd63874044ee49065
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347272"
---
# <span data-ttu-id="fde0f-101">Get-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="fde0f-101">Get-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="fde0f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fde0f-102">SYNOPSIS</span></span>
<span data-ttu-id="fde0f-103">Ottenere i metadati correlati non relativi alla sicurezza di un servizio di dispositivo Windows.</span><span class="sxs-lookup"><span data-stu-id="fde0f-103">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="fde0f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fde0f-104">SYNTAX</span></span>

### <span data-ttu-id="fde0f-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fde0f-105">List1 (Default)</span></span>
```
Get-AzWindowsIotServicesDevice [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fde0f-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="fde0f-106">Get</span></span>
```
Get-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fde0f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fde0f-107">GetViaIdentity</span></span>
```
Get-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="fde0f-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="fde0f-108">List</span></span>
```
Get-AzWindowsIotServicesDevice -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="fde0f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fde0f-109">DESCRIPTION</span></span>
<span data-ttu-id="fde0f-110">Ottenere i metadati correlati non relativi alla sicurezza di un servizio di dispositivo Windows.</span><span class="sxs-lookup"><span data-stu-id="fde0f-110">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="fde0f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fde0f-111">EXAMPLES</span></span>

### <span data-ttu-id="fde0f-112">Esempio 1: ottenere tutti i servizi Windows molto in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="fde0f-112">Example 1: Get all Windows IoT services under a subscription</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="fde0f-113">Questo comando consente di ottenere tutti i servizi Windows molto in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fde0f-113">This command gets all Windows IoT services under a subscription.</span></span>

### <span data-ttu-id="fde0f-114">Esempio 2: ottenere tutti i servizi Windows in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fde0f-114">Example 2: Get all Windows IoT services under a resource group</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="fde0f-115">Questo comando consente di ottenere tutti i servizi Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fde0f-115">This command gets all Windows IoT services under a resource group.</span></span>

### <span data-ttu-id="fde0f-116">Esempio 3: ottenere un servizio Windows molto per nome</span><span class="sxs-lookup"><span data-stu-id="fde0f-116">Example 3: Get a Windows IoT service by name</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="fde0f-117">Questo comando ottiene un servizio Windows molto per nome.</span><span class="sxs-lookup"><span data-stu-id="fde0f-117">This command gets a Windows IoT service by name.</span></span>

### <span data-ttu-id="fde0f-118">Esempio 4: ottenere un servizio Windows molto per oggetto</span><span class="sxs-lookup"><span data-stu-id="fde0f-118">Example 4: Get a Windows IoT service by object</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'
PS C:\> Get-AzWindowsIotServicesDevice -InputObject $wsi

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="fde0f-119">Questo comando ottiene un servizio Windows un sacco di oggetti.</span><span class="sxs-lookup"><span data-stu-id="fde0f-119">This command gets a Windows IoT service by object.</span></span>

### <span data-ttu-id="fde0f-120">Esempio 4: ottenere un servizio Windows molto per pipeline</span><span class="sxs-lookup"><span data-stu-id="fde0f-120">Example 4: Get a Windows IoT service by pipeline</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com' | Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="fde0f-121">Questo comando ottiene un servizio Windows molto per pipeline.</span><span class="sxs-lookup"><span data-stu-id="fde0f-121">This command gets a Windows IoT service by pipeline.</span></span>

## <span data-ttu-id="fde0f-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fde0f-122">PARAMETERS</span></span>

### <span data-ttu-id="fde0f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fde0f-123">-DefaultProfile</span></span>
<span data-ttu-id="fde0f-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fde0f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fde0f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fde0f-125">-InputObject</span></span>
<span data-ttu-id="fde0f-126">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="fde0f-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fde0f-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="fde0f-127">-Name</span></span>
<span data-ttu-id="fde0f-128">Nome del servizio di dispositivo Windows sacco.</span><span class="sxs-lookup"><span data-stu-id="fde0f-128">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="fde0f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fde0f-129">-ResourceGroupName</span></span>
<span data-ttu-id="fde0f-130">Il nome del gruppo di risorse che contiene il servizio Windows sacco.</span><span class="sxs-lookup"><span data-stu-id="fde0f-130">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="fde0f-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fde0f-131">-SubscriptionId</span></span>
<span data-ttu-id="fde0f-132">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fde0f-132">The subscription identifier.</span></span>

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

### <span data-ttu-id="fde0f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fde0f-133">CommonParameters</span></span>
<span data-ttu-id="fde0f-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fde0f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fde0f-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fde0f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fde0f-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fde0f-136">INPUTS</span></span>

### <span data-ttu-id="fde0f-137">Microsoft. Azure. PowerShell. Cmdlets. WindowsIotServices. Models. IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="fde0f-137">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="fde0f-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fde0f-138">OUTPUTS</span></span>

### <span data-ttu-id="fde0f-139">Microsoft. Azure. PowerShell. Cmdlets. WindowsIotServices. Models. Api20190601. IDeviceService</span><span class="sxs-lookup"><span data-stu-id="fde0f-139">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="fde0f-140">Note</span><span class="sxs-lookup"><span data-stu-id="fde0f-140">NOTES</span></span>

<span data-ttu-id="fde0f-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="fde0f-141">ALIASES</span></span>

<span data-ttu-id="fde0f-142">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fde0f-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fde0f-143">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="fde0f-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fde0f-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fde0f-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fde0f-145">INPUTOBJECT <IWindowsIotServicesIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="fde0f-145">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fde0f-146">`[DeviceName <String>]`: Nome del servizio Windows sacco.</span><span class="sxs-lookup"><span data-stu-id="fde0f-146">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="fde0f-147">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="fde0f-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fde0f-148">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene il servizio dispositivi Windows.</span><span class="sxs-lookup"><span data-stu-id="fde0f-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="fde0f-149">`[SubscriptionId <String>]`: Identificatore della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="fde0f-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="fde0f-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fde0f-150">RELATED LINKS</span></span>

