---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/powershell/module/az.windowsiotservices/update-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 27eecabc9bb144270b86a26e5128b9a0d63d346b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971582"
---
# <span data-ttu-id="24721-101">Update-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="24721-101">Update-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="24721-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24721-102">SYNOPSIS</span></span>
<span data-ttu-id="24721-103">Aggiorna i metadati di un servizio dispositivi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="24721-103">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="24721-104">Il modello più comune per modificare una proprietà è recuperare i metadati e i metadati di sicurezza di Windows IoT Device Service e quindi combinarli con i valori modificati in un nuovo corpo per aggiornare il servizio dispositivi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="24721-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="24721-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24721-105">SYNTAX</span></span>

### <span data-ttu-id="24721-106">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="24721-106">UpdateExpanded (Default)</span></span>
```
Update-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="24721-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="24721-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-IfMatch <String>]
 [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>] [-Location <String>]
 [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="24721-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="24721-108">DESCRIPTION</span></span>
<span data-ttu-id="24721-109">Aggiorna i metadati di un servizio dispositivi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="24721-109">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="24721-110">Il modello più comune per modificare una proprietà è recuperare i metadati e i metadati di sicurezza di Windows IoT Device Service e quindi combinarli con i valori modificati in un nuovo corpo per aggiornare il servizio dispositivi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="24721-110">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="24721-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24721-111">EXAMPLES</span></span>

### <span data-ttu-id="24721-112">Esempio 1: Aggiornare un servizio IoT di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="24721-112">Example 1: Update a Windows IoT services by name</span></span>
```powershell
PS C:\> Update-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Quantity 10

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "5d006a5c-0000-0700-0000-5faa46760000"
```

<span data-ttu-id="24721-113">Questo comando aggiorna i servizi Windows IoT in base al nome.</span><span class="sxs-lookup"><span data-stu-id="24721-113">This command updates a Windows IoT services by name.</span></span>

### <span data-ttu-id="24721-114">Esempio 2: Aggiornare un servizio IoT di Windows tramite pipeline</span><span class="sxs-lookup"><span data-stu-id="24721-114">Example 2: Update a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test | Update-AzWindowsIotServicesDevice-Quantity 100 -Tag @{'oper'='update'}

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5d005f5f-0000-0700-0000-5faa46ae0000"
```

<span data-ttu-id="24721-115">Questo comando aggiorna i servizi IoT di Windows tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="24721-115">This command updates a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="24721-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24721-116">PARAMETERS</span></span>

### <span data-ttu-id="24721-117">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="24721-117">-AdminDomainName</span></span>
<span data-ttu-id="24721-118">Dominio OEM AAD del servizio dispositivi Windows IoT</span><span class="sxs-lookup"><span data-stu-id="24721-118">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="24721-119">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="24721-119">-BillingDomainName</span></span>
<span data-ttu-id="24721-120">Dominio AAD del servizio ODM per dispositivi Windows IoT</span><span class="sxs-lookup"><span data-stu-id="24721-120">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="24721-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24721-121">-DefaultProfile</span></span>
<span data-ttu-id="24721-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24721-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24721-123">-Etag</span><span class="sxs-lookup"><span data-stu-id="24721-123">-Etag</span></span>
<span data-ttu-id="24721-124">Il campo Etag non *è* obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="24721-124">The Etag field is *not* required.</span></span>
<span data-ttu-id="24721-125">Se viene fornito nel corpo della risposta, deve anche essere fornito come intestazione in base alla normale convenzione ETag.</span><span class="sxs-lookup"><span data-stu-id="24721-125">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="24721-126">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="24721-126">-IfMatch</span></span>
<span data-ttu-id="24721-127">ETag del servizio dispositivi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="24721-127">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="24721-128">Non specificare per la creazione di un nuovo servizio dispositivi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="24721-128">Do not specify for creating a brand new Windows IoT Device Service.</span></span>
<span data-ttu-id="24721-129">Necessario per aggiornare un servizio dispositivi Windows IoT esistente.</span><span class="sxs-lookup"><span data-stu-id="24721-129">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="24721-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24721-130">-InputObject</span></span>
<span data-ttu-id="24721-131">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="24721-131">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="24721-132">-Location</span><span class="sxs-lookup"><span data-stu-id="24721-132">-Location</span></span>
<span data-ttu-id="24721-133">Area geografica di Azure in cui si trova la risorsa</span><span class="sxs-lookup"><span data-stu-id="24721-133">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="24721-134">-Name</span><span class="sxs-lookup"><span data-stu-id="24721-134">-Name</span></span>
<span data-ttu-id="24721-135">Nome del servizio di dispositivi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="24721-135">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="24721-136">-Nota</span><span class="sxs-lookup"><span data-stu-id="24721-136">-Note</span></span>
<span data-ttu-id="24721-137">Note di Windows IoT Device Service.</span><span class="sxs-lookup"><span data-stu-id="24721-137">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="24721-138">-Quantity</span><span class="sxs-lookup"><span data-stu-id="24721-138">-Quantity</span></span>
<span data-ttu-id="24721-139">Allocazione del dispositivo Servizio dispositivi IoT di Windows,</span><span class="sxs-lookup"><span data-stu-id="24721-139">Windows IoT Device Service device allocation,</span></span>

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

### <span data-ttu-id="24721-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24721-140">-ResourceGroupName</span></span>
<span data-ttu-id="24721-141">Nome del gruppo di risorse che contiene il servizio di dispositivi IoT di Windows.</span><span class="sxs-lookup"><span data-stu-id="24721-141">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="24721-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24721-142">-SubscriptionId</span></span>
<span data-ttu-id="24721-143">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="24721-143">The subscription identifier.</span></span>

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

### <span data-ttu-id="24721-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="24721-144">-Tag</span></span>
<span data-ttu-id="24721-145">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="24721-145">Resource tags.</span></span>

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

### <span data-ttu-id="24721-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24721-146">-Confirm</span></span>
<span data-ttu-id="24721-147">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24721-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24721-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24721-148">-WhatIf</span></span>
<span data-ttu-id="24721-149">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24721-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24721-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24721-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24721-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24721-151">CommonParameters</span></span>
<span data-ttu-id="24721-152">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24721-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24721-153">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="24721-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24721-154">INPUT</span><span class="sxs-lookup"><span data-stu-id="24721-154">INPUTS</span></span>

### <span data-ttu-id="24721-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="24721-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="24721-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24721-156">OUTPUTS</span></span>

### <span data-ttu-id="24721-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="24721-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="24721-158">NOTE</span><span class="sxs-lookup"><span data-stu-id="24721-158">NOTES</span></span>

<span data-ttu-id="24721-159">ALIAS</span><span class="sxs-lookup"><span data-stu-id="24721-159">ALIASES</span></span>

<span data-ttu-id="24721-160">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="24721-160">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="24721-161">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="24721-161">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="24721-162">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="24721-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="24721-163">INPUTOBJECT <IWindowsIotServicesIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="24721-163">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="24721-164">`[DeviceName <String>]`: nome del servizio dispositivi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="24721-164">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="24721-165">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="24721-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="24721-166">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il servizio dispositivi IoT di Windows.</span><span class="sxs-lookup"><span data-stu-id="24721-166">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="24721-167">`[SubscriptionId <String>]`: l'identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="24721-167">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="24721-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24721-168">RELATED LINKS</span></span>

