---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: a00eb5977ad1a58b12ad3f326d36dba8d083d718
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688045"
---
# <span data-ttu-id="d9be6-101">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9be6-101">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="d9be6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9be6-102">SYNOPSIS</span></span>
<span data-ttu-id="d9be6-103">Aggiunge informazioni di intestazione personalizzate a un oggetto endpoint di gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="d9be6-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9be6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9be6-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9be6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9be6-105">DESCRIPTION</span></span>
<span data-ttu-id="d9be6-106">Il cmdlet **Add-AzureRmTrafficManagerCustomHeaderToEndpoint** aggiunge informazioni di intestazione personalizzate a un oggetto endpoint di Azure Traffic Manager locale.</span><span class="sxs-lookup"><span data-stu-id="d9be6-106">The **Add-AzureRmTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="d9be6-107">Puoi ottenere un endpoint usando i cmdlet New-AzureRmTrafficManagerEndpoint o Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d9be6-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="d9be6-108">Questo cmdlet funziona sull'oggetto endpoint locale.</span><span class="sxs-lookup"><span data-stu-id="d9be6-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="d9be6-109">Eseguire il commit delle modifiche apportate all'endpoint per Traffic Manager usando il cmdlet Set-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d9be6-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="d9be6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9be6-110">EXAMPLES</span></span>

### <span data-ttu-id="d9be6-111">Esempio 1: aggiungere informazioni di intestazione personalizzate a un endpoint</span><span class="sxs-lookup"><span data-stu-id="d9be6-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzureRmTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="d9be6-112">Con il primo comando viene creato un endpoint di Azure Traffic Manager usando il cmdlet **New-AzureRmTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="d9be6-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="d9be6-113">Il comando Archivia l'endpoint locale nella variabile $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d9be6-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="d9be6-114">Il secondo comando aggiunge informazioni di intestazione personalizzate all'endpoint archiviato in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d9be6-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="d9be6-115">Il comando finale aggiorna l'endpoint in gestione traffico per corrispondere al valore locale in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d9be6-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="d9be6-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9be6-116">PARAMETERS</span></span>

### <span data-ttu-id="d9be6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9be6-117">-DefaultProfile</span></span>
<span data-ttu-id="d9be6-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9be6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9be6-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9be6-119">-Name</span></span>
<span data-ttu-id="d9be6-120">Specifica il nome delle informazioni di intestazione personalizzate da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="d9be6-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="d9be6-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9be6-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="d9be6-122">Specifica un oggetto **TrafficManagerEndpoint** locale.</span><span class="sxs-lookup"><span data-stu-id="d9be6-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="d9be6-123">Questo cmdlet modifica questo oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="d9be6-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="d9be6-124">Per ottenere un oggetto **TrafficManagerEndpoint** , usa il cmdlet Get-AzureRmTrafficManagerEndpoint o New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d9be6-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9be6-125">-Valore</span><span class="sxs-lookup"><span data-stu-id="d9be6-125">-Value</span></span>
<span data-ttu-id="d9be6-126">Specifica il valore delle informazioni di intestazione personalizzate da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="d9be6-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="d9be6-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d9be6-127">-Confirm</span></span>
<span data-ttu-id="d9be6-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9be6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9be6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9be6-129">-WhatIf</span></span>
<span data-ttu-id="d9be6-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9be6-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9be6-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9be6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9be6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9be6-132">CommonParameters</span></span>
<span data-ttu-id="d9be6-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9be6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9be6-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9be6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9be6-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9be6-135">INPUTS</span></span>

### <span data-ttu-id="d9be6-136">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9be6-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="d9be6-137">Questo cmdlet accetta un oggetto **TrafficManagerEndpoint** per questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9be6-137">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="d9be6-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9be6-138">OUTPUTS</span></span>

### <span data-ttu-id="d9be6-139">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9be6-139">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="d9be6-140">Questo cmdlet restituisce un oggetto **TrafficManagerEndpoint** modificato.</span><span class="sxs-lookup"><span data-stu-id="d9be6-140">This cmdlet returns a modified **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="d9be6-141">Note</span><span class="sxs-lookup"><span data-stu-id="d9be6-141">NOTES</span></span>

## <span data-ttu-id="d9be6-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9be6-142">RELATED LINKS</span></span>

[<span data-ttu-id="d9be6-143">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9be6-143">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="d9be6-144">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9be6-144">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="d9be6-145">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d9be6-145">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="d9be6-146">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9be6-146">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
