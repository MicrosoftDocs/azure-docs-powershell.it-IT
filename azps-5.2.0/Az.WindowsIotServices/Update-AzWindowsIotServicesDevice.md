---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/update-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 5e50ad3dc1ce2396dfb7a2b498efc82c4e95e430
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371461"
---
# <span data-ttu-id="2a954-101">Update-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="2a954-101">Update-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="2a954-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2a954-102">SYNOPSIS</span></span>
<span data-ttu-id="2a954-103">Aggiorna i metadati di un servizio per dispositivi Windows.</span><span class="sxs-lookup"><span data-stu-id="2a954-103">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="2a954-104">Il modello usuale per la modifica di una proprietà consiste nel recuperare i metadati del servizio di dispositivo Windows e i metadati di sicurezza e quindi combinarli con i valori modificati in un nuovo corpo per aggiornare il servizio Windows sacco.</span><span class="sxs-lookup"><span data-stu-id="2a954-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="2a954-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a954-105">SYNTAX</span></span>

### <span data-ttu-id="2a954-106">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2a954-106">UpdateExpanded (Default)</span></span>
```
Update-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2a954-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2a954-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-IfMatch <String>]
 [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>] [-Location <String>]
 [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="2a954-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a954-108">DESCRIPTION</span></span>
<span data-ttu-id="2a954-109">Aggiorna i metadati di un servizio per dispositivi Windows.</span><span class="sxs-lookup"><span data-stu-id="2a954-109">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="2a954-110">Il modello usuale per la modifica di una proprietà consiste nel recuperare i metadati del servizio di dispositivo Windows e i metadati di sicurezza e quindi combinarli con i valori modificati in un nuovo corpo per aggiornare il servizio Windows sacco.</span><span class="sxs-lookup"><span data-stu-id="2a954-110">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="2a954-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a954-111">EXAMPLES</span></span>

### <span data-ttu-id="2a954-112">Esempio 1: aggiornare un servizio Windows per nome</span><span class="sxs-lookup"><span data-stu-id="2a954-112">Example 1: Update a Windows IoT services by name</span></span>
```powershell
PS C:\> Update-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Quantity 10

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "5d006a5c-0000-0700-0000-5faa46760000"
```

<span data-ttu-id="2a954-113">Questo comando aggiorna un servizio Windows per nome.</span><span class="sxs-lookup"><span data-stu-id="2a954-113">This command updates a Windows IoT services by name.</span></span>

### <span data-ttu-id="2a954-114">Esempio 2: aggiornare un servizio Windows un sacco di servizi per pipeline</span><span class="sxs-lookup"><span data-stu-id="2a954-114">Example 2: Update a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test | Update-AzWindowsIotServicesDevice-Quantity 100 -Tag @{'oper'='update'}

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5d005f5f-0000-0700-0000-5faa46ae0000"
```

<span data-ttu-id="2a954-115">Questo comando aggiorna un servizio Windows un sacco di servizi per pipeline.</span><span class="sxs-lookup"><span data-stu-id="2a954-115">This command updates a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="2a954-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a954-116">PARAMETERS</span></span>

### <span data-ttu-id="2a954-117">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="2a954-117">-AdminDomainName</span></span>
<span data-ttu-id="2a954-118">Domain Service OEM AAD di Windows per dispositivi</span><span class="sxs-lookup"><span data-stu-id="2a954-118">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="2a954-119">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="2a954-119">-BillingDomainName</span></span>
<span data-ttu-id="2a954-120">Domain Service ODM AAD di Windows sacco</span><span class="sxs-lookup"><span data-stu-id="2a954-120">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="2a954-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a954-121">-DefaultProfile</span></span>
<span data-ttu-id="2a954-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a954-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a954-123">-ETag</span><span class="sxs-lookup"><span data-stu-id="2a954-123">-Etag</span></span>
<span data-ttu-id="2a954-124">Il campo ETag *non* è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2a954-124">The Etag field is *not* required.</span></span>
<span data-ttu-id="2a954-125">Se viene fornito nel corpo della risposta, deve essere fornito anche come intestazione per la normale convenzione ETag.</span><span class="sxs-lookup"><span data-stu-id="2a954-125">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="2a954-126">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="2a954-126">-IfMatch</span></span>
<span data-ttu-id="2a954-127">ETag del servizio Windows sacco.</span><span class="sxs-lookup"><span data-stu-id="2a954-127">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="2a954-128">Non specificare per la creazione di un nuovo servizio Windows sacco.</span><span class="sxs-lookup"><span data-stu-id="2a954-128">Do not specify for creating a brand new Windows IoT Device Service.</span></span>
<span data-ttu-id="2a954-129">Necessario per aggiornare un servizio Windows.</span><span class="sxs-lookup"><span data-stu-id="2a954-129">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="2a954-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a954-130">-InputObject</span></span>
<span data-ttu-id="2a954-131">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2a954-131">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a954-132">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2a954-132">-Location</span></span>
<span data-ttu-id="2a954-133">Area di Azure in cui vive la risorsa</span><span class="sxs-lookup"><span data-stu-id="2a954-133">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="2a954-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a954-134">-Name</span></span>
<span data-ttu-id="2a954-135">Nome del servizio di dispositivo Windows sacco.</span><span class="sxs-lookup"><span data-stu-id="2a954-135">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a954-136">-Nota</span><span class="sxs-lookup"><span data-stu-id="2a954-136">-Note</span></span>
<span data-ttu-id="2a954-137">Note del servizio Windows sacco di dispositivi.</span><span class="sxs-lookup"><span data-stu-id="2a954-137">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="2a954-138">-Quantità</span><span class="sxs-lookup"><span data-stu-id="2a954-138">-Quantity</span></span>
<span data-ttu-id="2a954-139">Allocazione del dispositivo Windows sacco di servizi</span><span class="sxs-lookup"><span data-stu-id="2a954-139">Windows IoT Device Service device allocation,</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a954-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a954-140">-ResourceGroupName</span></span>
<span data-ttu-id="2a954-141">Il nome del gruppo di risorse che contiene il servizio Windows sacco.</span><span class="sxs-lookup"><span data-stu-id="2a954-141">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a954-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2a954-142">-SubscriptionId</span></span>
<span data-ttu-id="2a954-143">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2a954-143">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a954-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="2a954-144">-Tag</span></span>
<span data-ttu-id="2a954-145">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="2a954-145">Resource tags.</span></span>

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

### <span data-ttu-id="2a954-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2a954-146">-Confirm</span></span>
<span data-ttu-id="2a954-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a954-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a954-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a954-148">-WhatIf</span></span>
<span data-ttu-id="2a954-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a954-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a954-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a954-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a954-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a954-151">CommonParameters</span></span>
<span data-ttu-id="2a954-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a954-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a954-153">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a954-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a954-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2a954-154">INPUTS</span></span>

### <span data-ttu-id="2a954-155">Microsoft. Azure. PowerShell. Cmdlets. WindowsIotServices. Models. IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="2a954-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="2a954-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a954-156">OUTPUTS</span></span>

### <span data-ttu-id="2a954-157">Microsoft. Azure. PowerShell. Cmdlets. WindowsIotServices. Models. Api20190601. IDeviceService</span><span class="sxs-lookup"><span data-stu-id="2a954-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="2a954-158">Note</span><span class="sxs-lookup"><span data-stu-id="2a954-158">NOTES</span></span>

<span data-ttu-id="2a954-159">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2a954-159">ALIASES</span></span>

<span data-ttu-id="2a954-160">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a954-160">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2a954-161">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="2a954-161">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2a954-162">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2a954-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2a954-163">INPUTOBJECT <IWindowsIotServicesIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="2a954-163">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2a954-164">`[DeviceName <String>]`: Nome del servizio Windows sacco.</span><span class="sxs-lookup"><span data-stu-id="2a954-164">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="2a954-165">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="2a954-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2a954-166">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene il servizio dispositivi Windows.</span><span class="sxs-lookup"><span data-stu-id="2a954-166">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="2a954-167">`[SubscriptionId <String>]`: Identificatore della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="2a954-167">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="2a954-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a954-168">RELATED LINKS</span></span>

