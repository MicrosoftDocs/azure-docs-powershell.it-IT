---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: d5b7a2d0713fec7c11f33d778cf9708c253f153a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965917"
---
# <span data-ttu-id="e11a5-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="e11a5-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="e11a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e11a5-102">SYNOPSIS</span></span>
<span data-ttu-id="e11a5-103">Creare un oggetto PSBackend</span><span class="sxs-lookup"><span data-stu-id="e11a5-103">Create a PSBackend object</span></span>

## <span data-ttu-id="e11a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e11a5-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e11a5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e11a5-105">DESCRIPTION</span></span>
<span data-ttu-id="e11a5-106">Creare un oggetto PSBackend per la creazione della porta anteriore</span><span class="sxs-lookup"><span data-stu-id="e11a5-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="e11a5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e11a5-107">EXAMPLES</span></span>

### <span data-ttu-id="e11a5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e11a5-108">Example 1</span></span>
```powershell
PS C:\>New-AzFrontDoorBackendObject -Address "contoso1.azurewebsites.net"


Address           : contoso1.azurewebsites.net
HttpPort          : 80
HttpsPort         : 443
Priority          : 1
Weight            : 50
BackendHostHeader :
EnabledState      : Enabled
```

<span data-ttu-id="e11a5-109">Creare un oggetto PSBackend per la creazione della porta anteriore</span><span class="sxs-lookup"><span data-stu-id="e11a5-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="e11a5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e11a5-110">PARAMETERS</span></span>

### <span data-ttu-id="e11a5-111">-Address</span><span class="sxs-lookup"><span data-stu-id="e11a5-111">-Address</span></span>
<span data-ttu-id="e11a5-112">Posizione del back-end (indirizzo IP o FQDN)</span><span class="sxs-lookup"><span data-stu-id="e11a5-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="e11a5-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="e11a5-113">-BackendHostHeader</span></span>
<span data-ttu-id="e11a5-114">Valore da usare come intestazione host inviata al back-end.</span><span class="sxs-lookup"><span data-stu-id="e11a5-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="e11a5-115">Il valore predefinito è l'indirizzo back-end.</span><span class="sxs-lookup"><span data-stu-id="e11a5-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="e11a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e11a5-116">-DefaultProfile</span></span>
<span data-ttu-id="e11a5-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e11a5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e11a5-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="e11a5-118">-EnabledState</span></span>
<span data-ttu-id="e11a5-119">Se abilitare o meno l'uso di questo back-end.</span><span class="sxs-lookup"><span data-stu-id="e11a5-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="e11a5-120">Il valore predefinito è Abilitato</span><span class="sxs-lookup"><span data-stu-id="e11a5-120">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e11a5-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="e11a5-121">-HttpPort</span></span>
<span data-ttu-id="e11a5-122">Numero di porta TCP HTTP.</span><span class="sxs-lookup"><span data-stu-id="e11a5-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="e11a5-123">Deve essere compreso tra 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="e11a5-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="e11a5-124">Il valore predefinito è 80.</span><span class="sxs-lookup"><span data-stu-id="e11a5-124">Default value is 80.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e11a5-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="e11a5-125">-HttpsPort</span></span>
<span data-ttu-id="e11a5-126">Numero di porta TCP HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e11a5-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="e11a5-127">Deve essere compreso tra 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="e11a5-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="e11a5-128">Il valore predefinito è 443</span><span class="sxs-lookup"><span data-stu-id="e11a5-128">Default value is 443</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e11a5-129">-Priority</span><span class="sxs-lookup"><span data-stu-id="e11a5-129">-Priority</span></span>
<span data-ttu-id="e11a5-130">Priorità da usare per il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e11a5-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="e11a5-131">Deve essere compreso tra 1 e 5.</span><span class="sxs-lookup"><span data-stu-id="e11a5-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="e11a5-132">Il valore predefinito è 1</span><span class="sxs-lookup"><span data-stu-id="e11a5-132">Default value is 1</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e11a5-133">-PrivateLinkAlias</span><span class="sxs-lookup"><span data-stu-id="e11a5-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="e11a5-134">Alias della risorsa Collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="e11a5-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="e11a5-135">La compilazione di questo campo facoltativo indica che il back-end è 'Privato'</span><span class="sxs-lookup"><span data-stu-id="e11a5-135">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="e11a5-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="e11a5-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="e11a5-137">Messaggio personalizzato da includere nella richiesta di approvazione per la connessione al collegamento privato</span><span class="sxs-lookup"><span data-stu-id="e11a5-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

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

### <span data-ttu-id="e11a5-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="e11a5-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="e11a5-139">Posizione della risorsa Collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="e11a5-139">The Location of Private Link resource.</span></span> <span data-ttu-id="e11a5-140">Location è obbligatorio quando PrivateLinkResourceId è impostato</span><span class="sxs-lookup"><span data-stu-id="e11a5-140">Location is required when PrivateLinkResourceId is set</span></span>

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

### <span data-ttu-id="e11a5-141">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="e11a5-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="e11a5-142">ID risorsa del collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="e11a5-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="e11a5-143">La compilazione di questo campo facoltativo indica che il back-end è 'Privato'</span><span class="sxs-lookup"><span data-stu-id="e11a5-143">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="e11a5-144">-Spessore</span><span class="sxs-lookup"><span data-stu-id="e11a5-144">-Weight</span></span>
<span data-ttu-id="e11a5-145">Peso di questo endpoint a scopo di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e11a5-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="e11a5-146">Deve essere compreso tra 1 e 1000.</span><span class="sxs-lookup"><span data-stu-id="e11a5-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="e11a5-147">Il valore predefinito è 50</span><span class="sxs-lookup"><span data-stu-id="e11a5-147">Default value is 50</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e11a5-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e11a5-148">CommonParameters</span></span>
<span data-ttu-id="e11a5-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e11a5-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e11a5-150">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e11a5-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e11a5-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="e11a5-151">INPUTS</span></span>

### <span data-ttu-id="e11a5-152">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e11a5-152">None</span></span>

## <span data-ttu-id="e11a5-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e11a5-153">OUTPUTS</span></span>

### <span data-ttu-id="e11a5-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span><span class="sxs-lookup"><span data-stu-id="e11a5-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="e11a5-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="e11a5-155">NOTES</span></span>

## <span data-ttu-id="e11a5-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e11a5-156">RELATED LINKS</span></span>

[<span data-ttu-id="e11a5-157">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="e11a5-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
