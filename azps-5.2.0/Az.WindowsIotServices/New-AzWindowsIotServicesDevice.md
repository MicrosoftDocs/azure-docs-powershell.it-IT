---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/new-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 4da60a6d4083992f843121cb141a453b4ef3b4b8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347284"
---
# <span data-ttu-id="e827c-101">New-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="e827c-101">New-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="e827c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e827c-102">SYNOPSIS</span></span>
<span data-ttu-id="e827c-103">Creare o aggiornare i metadati di un servizio per dispositivi Windows.</span><span class="sxs-lookup"><span data-stu-id="e827c-103">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="e827c-104">Il modello usuale per la modifica di una proprietà consiste nel recuperare i metadati del servizio di dispositivo Windows e i metadati di sicurezza e quindi combinarli con i valori modificati in un nuovo corpo per aggiornare il servizio Windows sacco.</span><span class="sxs-lookup"><span data-stu-id="e827c-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="e827c-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e827c-105">SYNTAX</span></span>

```
New-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e827c-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e827c-106">DESCRIPTION</span></span>
<span data-ttu-id="e827c-107">Creare o aggiornare i metadati di un servizio per dispositivi Windows.</span><span class="sxs-lookup"><span data-stu-id="e827c-107">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="e827c-108">Il modello usuale per la modifica di una proprietà consiste nel recuperare i metadati del servizio di dispositivo Windows e i metadati di sicurezza e quindi combinarli con i valori modificati in un nuovo corpo per aggiornare il servizio Windows sacco.</span><span class="sxs-lookup"><span data-stu-id="e827c-108">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="e827c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e827c-109">EXAMPLES</span></span>

### <span data-ttu-id="e827c-110">Esempio 1: creare nuovi servizi Windows</span><span class="sxs-lookup"><span data-stu-id="e827c-110">Example 1: Create a new Windows IoT services</span></span>
```powershell
PS C:\> New-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "6a00eee9-0000-0700-0000-5fab82870000"
```

<span data-ttu-id="e827c-111">Questo comando crea un nuovo servizio Windows.</span><span class="sxs-lookup"><span data-stu-id="e827c-111">This command creates a new Windows IoT services.</span></span>

## <span data-ttu-id="e827c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e827c-112">PARAMETERS</span></span>

### <span data-ttu-id="e827c-113">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="e827c-113">-AdminDomainName</span></span>
<span data-ttu-id="e827c-114">Domain Service OEM AAD di Windows per dispositivi</span><span class="sxs-lookup"><span data-stu-id="e827c-114">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="e827c-115">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="e827c-115">-BillingDomainName</span></span>
<span data-ttu-id="e827c-116">Domain Service ODM AAD di Windows sacco</span><span class="sxs-lookup"><span data-stu-id="e827c-116">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="e827c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e827c-117">-DefaultProfile</span></span>
<span data-ttu-id="e827c-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e827c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e827c-119">-ETag</span><span class="sxs-lookup"><span data-stu-id="e827c-119">-Etag</span></span>
<span data-ttu-id="e827c-120">Il campo ETag *non* è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e827c-120">The Etag field is *not* required.</span></span>
<span data-ttu-id="e827c-121">Se viene fornito nel corpo della risposta, deve essere fornito anche come intestazione per la normale convenzione ETag.</span><span class="sxs-lookup"><span data-stu-id="e827c-121">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="e827c-122">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="e827c-122">-IfMatch</span></span>
<span data-ttu-id="e827c-123">ETag del servizio Windows sacco.</span><span class="sxs-lookup"><span data-stu-id="e827c-123">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="e827c-124">Non specificare per la creazione di un nuovo servizio Windows sacco di dispositivi.</span><span class="sxs-lookup"><span data-stu-id="e827c-124">Do not specify for creating a new Windows IoT Device Service.</span></span>
<span data-ttu-id="e827c-125">Necessario per aggiornare un servizio Windows.</span><span class="sxs-lookup"><span data-stu-id="e827c-125">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="e827c-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e827c-126">-Location</span></span>
<span data-ttu-id="e827c-127">Area di Azure in cui vive la risorsa</span><span class="sxs-lookup"><span data-stu-id="e827c-127">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="e827c-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e827c-128">-Name</span></span>
<span data-ttu-id="e827c-129">Nome del servizio di dispositivo Windows sacco.</span><span class="sxs-lookup"><span data-stu-id="e827c-129">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="e827c-130">-Nota</span><span class="sxs-lookup"><span data-stu-id="e827c-130">-Note</span></span>
<span data-ttu-id="e827c-131">Note del servizio Windows sacco di dispositivi.</span><span class="sxs-lookup"><span data-stu-id="e827c-131">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="e827c-132">-Quantità</span><span class="sxs-lookup"><span data-stu-id="e827c-132">-Quantity</span></span>
<span data-ttu-id="e827c-133">Allocazione del dispositivo Windows sacco di servizi</span><span class="sxs-lookup"><span data-stu-id="e827c-133">Windows IoT Device Service device allocation,</span></span>

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

### <span data-ttu-id="e827c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e827c-134">-ResourceGroupName</span></span>
<span data-ttu-id="e827c-135">Il nome del gruppo di risorse che contiene il servizio Windows sacco.</span><span class="sxs-lookup"><span data-stu-id="e827c-135">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="e827c-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e827c-136">-SubscriptionId</span></span>
<span data-ttu-id="e827c-137">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="e827c-137">The subscription identifier.</span></span>

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

### <span data-ttu-id="e827c-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="e827c-138">-Tag</span></span>
<span data-ttu-id="e827c-139">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="e827c-139">Resource tags.</span></span>

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

### <span data-ttu-id="e827c-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e827c-140">-Confirm</span></span>
<span data-ttu-id="e827c-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e827c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e827c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e827c-142">-WhatIf</span></span>
<span data-ttu-id="e827c-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e827c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e827c-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e827c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e827c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e827c-145">CommonParameters</span></span>
<span data-ttu-id="e827c-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e827c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e827c-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e827c-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e827c-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e827c-148">INPUTS</span></span>

## <span data-ttu-id="e827c-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e827c-149">OUTPUTS</span></span>

### <span data-ttu-id="e827c-150">Microsoft. Azure. PowerShell. Cmdlets. WindowsIotServices. Models. Api20190601. IDeviceService</span><span class="sxs-lookup"><span data-stu-id="e827c-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="e827c-151">Note</span><span class="sxs-lookup"><span data-stu-id="e827c-151">NOTES</span></span>

<span data-ttu-id="e827c-152">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e827c-152">ALIASES</span></span>

## <span data-ttu-id="e827c-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e827c-153">RELATED LINKS</span></span>

