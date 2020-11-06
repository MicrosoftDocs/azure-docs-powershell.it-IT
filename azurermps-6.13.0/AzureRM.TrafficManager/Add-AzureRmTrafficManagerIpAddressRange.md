---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurermtrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerIpAddressRange.md
ms.openlocfilehash: 213e959ecfec178644246f56be11e5b7306ef07f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508991"
---
# <span data-ttu-id="e86b7-101">Add-AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="e86b7-101">Add-AzureRmTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="e86b7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e86b7-102">SYNOPSIS</span></span>
<span data-ttu-id="e86b7-103">Aggiunge un intervallo di indirizzi o una subnet a un oggetto endpoint di gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="e86b7-103">Adds an address range or subnet to a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e86b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e86b7-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e86b7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e86b7-105">DESCRIPTION</span></span>
<span data-ttu-id="e86b7-106">Il cmdlet **Add-AzureRmTrafficManagerIpAddressRange** aggiunge un intervallo di indirizzi IP a un oggetto endpoint di Azure Traffic Manager locale.</span><span class="sxs-lookup"><span data-stu-id="e86b7-106">The **Add-AzureRmTrafficManagerIpAddressRange** cmdlet adds an IP address range to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="e86b7-107">Puoi ottenere un endpoint usando i cmdlet New-AzureRmTrafficManagerEndpoint o Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e86b7-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="e86b7-108">Questo cmdlet funziona sull'oggetto endpoint locale.</span><span class="sxs-lookup"><span data-stu-id="e86b7-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="e86b7-109">Eseguire il commit delle modifiche apportate all'endpoint per Traffic Manager usando il cmdlet Set-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e86b7-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="e86b7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e86b7-110">EXAMPLES</span></span>

### <span data-ttu-id="e86b7-111">Esempio 1: aggiungere intervalli di indirizzi IP a un endpoint</span><span class="sxs-lookup"><span data-stu-id="e86b7-111">Example 1: Add IP address ranges to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="e86b7-112">Con il primo comando viene creato un endpoint di Azure Traffic Manager usando il cmdlet **New-AzureRmTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="e86b7-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="e86b7-113">Il comando Archivia l'endpoint locale nella variabile $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e86b7-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="e86b7-114">Il secondo comando aggiunge l'intervallo di indirizzi IP 1.2.3.4 a 5.6.7.8 all'endpoint archiviato in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e86b7-114">The second command adds the IP address range 1.2.3.4 to 5.6.7.8 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="e86b7-115">Il terzo comando aggiunge l'intervallo di indirizzi IP 9.10.11.0 a 9.10.11.255 all'endpoint archiviato in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e86b7-115">The third command adds the IP address range 9.10.11.0 to 9.10.11.255 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="e86b7-116">Il quarto comando verifica che l'ambito corrisponda alle dimensioni dell'intervallo, quindi aggiunge l'intervallo di indirizzi IP 12.13.14.0 a 12.13.14.31 all'endpoint archiviato in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e86b7-116">The fourth command verifies that the scope matches the size of the range, then adds the IP address range 12.13.14.0 to 12.13.14.31 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="e86b7-117">Il quinto comando aggiunge l'intervallo di indirizzi IP 15.16.17.18 a 15.16.17.18 all'endpoint archiviato in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e86b7-117">The fifth command adds the IP address range 15.16.17.18 to 15.16.17.18 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="e86b7-118">Il comando finale aggiorna l'endpoint in gestione traffico per corrispondere al valore locale in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e86b7-118">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="e86b7-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e86b7-119">PARAMETERS</span></span>

### <span data-ttu-id="e86b7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e86b7-120">-DefaultProfile</span></span>
<span data-ttu-id="e86b7-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e86b7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e86b7-122">-Last</span><span class="sxs-lookup"><span data-stu-id="e86b7-122">-Last</span></span>
<span data-ttu-id="e86b7-123">Specifica l'ultimo indirizzo IP nell'intervallo da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e86b7-123">Specifies the last IP address in the range to be added.</span></span>

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

### <span data-ttu-id="e86b7-124">-Ambito</span><span class="sxs-lookup"><span data-stu-id="e86b7-124">-Scope</span></span>
<span data-ttu-id="e86b7-125">Specifica l'ambito dell'intervallo di indirizzi IP da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e86b7-125">Specifies the scope of the IP address range to be added.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86b7-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e86b7-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="e86b7-127">Specifica un oggetto **TrafficManagerEndpoint** locale.</span><span class="sxs-lookup"><span data-stu-id="e86b7-127">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="e86b7-128">Questo cmdlet modifica questo oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="e86b7-128">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="e86b7-129">Per ottenere un oggetto **TrafficManagerEndpoint** , usa il cmdlet Get-AzureRmTrafficManagerEndpoint o New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e86b7-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="e86b7-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e86b7-130">-Confirm</span></span>
<span data-ttu-id="e86b7-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e86b7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e86b7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e86b7-132">-WhatIf</span></span>
<span data-ttu-id="e86b7-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e86b7-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e86b7-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e86b7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e86b7-135">-Primo</span><span class="sxs-lookup"><span data-stu-id="e86b7-135">-First</span></span>
<span data-ttu-id="e86b7-136">Specifica il primo indirizzo IP nell'intervallo da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e86b7-136">Specifies the first IP address in the range to be added.</span></span>

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

### <span data-ttu-id="e86b7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e86b7-137">CommonParameters</span></span>
<span data-ttu-id="e86b7-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e86b7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e86b7-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e86b7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e86b7-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e86b7-140">INPUTS</span></span>

### <span data-ttu-id="e86b7-141">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e86b7-141">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="e86b7-142">Questo cmdlet accetta un oggetto **TrafficManagerEndpoint** per questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e86b7-142">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="e86b7-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e86b7-143">OUTPUTS</span></span>

### <span data-ttu-id="e86b7-144">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e86b7-144">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="e86b7-145">Questo cmdlet restituisce un oggetto **TrafficManagerEndpoint** modificato.</span><span class="sxs-lookup"><span data-stu-id="e86b7-145">This cmdlet returns a modified **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="e86b7-146">Note</span><span class="sxs-lookup"><span data-stu-id="e86b7-146">NOTES</span></span>

## <span data-ttu-id="e86b7-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e86b7-147">RELATED LINKS</span></span>

[<span data-ttu-id="e86b7-148">Remove-AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="e86b7-148">Remove-AzureRmTrafficManagerIpAddressRange</span></span>](./Remove-AzureRmTrafficManagerIpAddressRange.md)

[<span data-ttu-id="e86b7-149">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e86b7-149">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="e86b7-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e86b7-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="e86b7-151">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e86b7-151">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
