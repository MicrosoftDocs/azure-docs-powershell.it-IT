---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/new-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 4da60a6d4083992f843121cb141a453b4ef3b4b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207403"
---
# <span data-ttu-id="29588-101">New-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="29588-101">New-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="29588-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29588-102">SYNOPSIS</span></span>
<span data-ttu-id="29588-103">Creare o aggiornare i metadati di un servizio dispositivi IoT di Windows.</span><span class="sxs-lookup"><span data-stu-id="29588-103">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="29588-104">Il modello più comune per modificare una proprietà è recuperare i metadati e i metadati di sicurezza di Windows IoT Device Service e quindi combinarli con i valori modificati in un nuovo corpo per aggiornare il servizio dispositivi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="29588-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="29588-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29588-105">SYNTAX</span></span>

```
New-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="29588-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="29588-106">DESCRIPTION</span></span>
<span data-ttu-id="29588-107">Creare o aggiornare i metadati di un servizio dispositivi IoT di Windows.</span><span class="sxs-lookup"><span data-stu-id="29588-107">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="29588-108">Il modello più comune per modificare una proprietà è recuperare i metadati e i metadati di sicurezza di Windows IoT Device Service e quindi combinarli con i valori modificati in un nuovo corpo per aggiornare il servizio dispositivi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="29588-108">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="29588-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29588-109">EXAMPLES</span></span>

### <span data-ttu-id="29588-110">Esempio 1: Creare nuovi servizi IoT di Windows</span><span class="sxs-lookup"><span data-stu-id="29588-110">Example 1: Create a new Windows IoT services</span></span>
```powershell
PS C:\> New-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "6a00eee9-0000-0700-0000-5fab82870000"
```

<span data-ttu-id="29588-111">Questo comando crea nuovi servizi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="29588-111">This command creates a new Windows IoT services.</span></span>

## <span data-ttu-id="29588-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29588-112">PARAMETERS</span></span>

### <span data-ttu-id="29588-113">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="29588-113">-AdminDomainName</span></span>
<span data-ttu-id="29588-114">Dominio OEM AAD del servizio dispositivi Windows IoT</span><span class="sxs-lookup"><span data-stu-id="29588-114">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="29588-115">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="29588-115">-BillingDomainName</span></span>
<span data-ttu-id="29588-116">Dominio AAD del servizio ODM per dispositivi Windows IoT</span><span class="sxs-lookup"><span data-stu-id="29588-116">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="29588-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29588-117">-DefaultProfile</span></span>
<span data-ttu-id="29588-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="29588-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29588-119">-Etag</span><span class="sxs-lookup"><span data-stu-id="29588-119">-Etag</span></span>
<span data-ttu-id="29588-120">Il campo Etag non *è* obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="29588-120">The Etag field is *not* required.</span></span>
<span data-ttu-id="29588-121">Se viene fornito nel corpo della risposta, deve anche essere fornito come intestazione in base alla normale convenzione ETag.</span><span class="sxs-lookup"><span data-stu-id="29588-121">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="29588-122">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="29588-122">-IfMatch</span></span>
<span data-ttu-id="29588-123">ETag del servizio dispositivi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="29588-123">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="29588-124">Non specificare per la creazione di un nuovo servizio dispositivi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="29588-124">Do not specify for creating a new Windows IoT Device Service.</span></span>
<span data-ttu-id="29588-125">Necessario per aggiornare un servizio dispositivi Windows IoT esistente.</span><span class="sxs-lookup"><span data-stu-id="29588-125">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="29588-126">-Location</span><span class="sxs-lookup"><span data-stu-id="29588-126">-Location</span></span>
<span data-ttu-id="29588-127">Area geografica di Azure in cui si trova la risorsa</span><span class="sxs-lookup"><span data-stu-id="29588-127">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="29588-128">-Name</span><span class="sxs-lookup"><span data-stu-id="29588-128">-Name</span></span>
<span data-ttu-id="29588-129">Nome del servizio di dispositivi Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="29588-129">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="29588-130">-Nota</span><span class="sxs-lookup"><span data-stu-id="29588-130">-Note</span></span>
<span data-ttu-id="29588-131">Note di Windows IoT Device Service.</span><span class="sxs-lookup"><span data-stu-id="29588-131">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="29588-132">-Quantity</span><span class="sxs-lookup"><span data-stu-id="29588-132">-Quantity</span></span>
<span data-ttu-id="29588-133">Allocazione del dispositivo Servizio dispositivi IoT di Windows,</span><span class="sxs-lookup"><span data-stu-id="29588-133">Windows IoT Device Service device allocation,</span></span>

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

### <span data-ttu-id="29588-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29588-134">-ResourceGroupName</span></span>
<span data-ttu-id="29588-135">Nome del gruppo di risorse che contiene il servizio di dispositivi IoT di Windows.</span><span class="sxs-lookup"><span data-stu-id="29588-135">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="29588-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="29588-136">-SubscriptionId</span></span>
<span data-ttu-id="29588-137">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="29588-137">The subscription identifier.</span></span>

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

### <span data-ttu-id="29588-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="29588-138">-Tag</span></span>
<span data-ttu-id="29588-139">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="29588-139">Resource tags.</span></span>

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

### <span data-ttu-id="29588-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29588-140">-Confirm</span></span>
<span data-ttu-id="29588-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29588-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29588-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29588-142">-WhatIf</span></span>
<span data-ttu-id="29588-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="29588-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29588-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="29588-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29588-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29588-145">CommonParameters</span></span>
<span data-ttu-id="29588-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29588-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29588-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="29588-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29588-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="29588-148">INPUTS</span></span>

## <span data-ttu-id="29588-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29588-149">OUTPUTS</span></span>

### <span data-ttu-id="29588-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="29588-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="29588-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="29588-151">NOTES</span></span>

<span data-ttu-id="29588-152">ALIAS</span><span class="sxs-lookup"><span data-stu-id="29588-152">ALIASES</span></span>

## <span data-ttu-id="29588-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29588-153">RELATED LINKS</span></span>

