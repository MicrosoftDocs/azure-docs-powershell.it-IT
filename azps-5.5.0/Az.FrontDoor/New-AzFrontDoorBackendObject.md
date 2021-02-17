---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 8eee112840fa7d7af81838927017b38988c9649b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188423"
---
# <span data-ttu-id="4074f-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="4074f-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="4074f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4074f-102">SYNOPSIS</span></span>
<span data-ttu-id="4074f-103">Creare un oggetto PSBackend</span><span class="sxs-lookup"><span data-stu-id="4074f-103">Create a PSBackend object</span></span>

## <span data-ttu-id="4074f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4074f-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4074f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4074f-105">DESCRIPTION</span></span>
<span data-ttu-id="4074f-106">Creare un oggetto PSBackend per la creazione della porta anteriore</span><span class="sxs-lookup"><span data-stu-id="4074f-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="4074f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4074f-107">EXAMPLES</span></span>

### <span data-ttu-id="4074f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4074f-108">Example 1</span></span>
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

<span data-ttu-id="4074f-109">Creare un oggetto PSBackend per la creazione della porta anteriore</span><span class="sxs-lookup"><span data-stu-id="4074f-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="4074f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4074f-110">PARAMETERS</span></span>

### <span data-ttu-id="4074f-111">-Address</span><span class="sxs-lookup"><span data-stu-id="4074f-111">-Address</span></span>
<span data-ttu-id="4074f-112">Posizione del back-end (indirizzo IP o FQDN)</span><span class="sxs-lookup"><span data-stu-id="4074f-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="4074f-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="4074f-113">-BackendHostHeader</span></span>
<span data-ttu-id="4074f-114">Valore da usare come intestazione host inviata al back-end.</span><span class="sxs-lookup"><span data-stu-id="4074f-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="4074f-115">Il valore predefinito è l'indirizzo back-end.</span><span class="sxs-lookup"><span data-stu-id="4074f-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="4074f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4074f-116">-DefaultProfile</span></span>
<span data-ttu-id="4074f-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4074f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4074f-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="4074f-118">-EnabledState</span></span>
<span data-ttu-id="4074f-119">Se abilitare o meno l'uso di questo back-end.</span><span class="sxs-lookup"><span data-stu-id="4074f-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="4074f-120">Il valore predefinito è Abilitato</span><span class="sxs-lookup"><span data-stu-id="4074f-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="4074f-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="4074f-121">-HttpPort</span></span>
<span data-ttu-id="4074f-122">Numero di porta TCP HTTP.</span><span class="sxs-lookup"><span data-stu-id="4074f-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="4074f-123">Deve essere compreso tra 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="4074f-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="4074f-124">Il valore predefinito è 80.</span><span class="sxs-lookup"><span data-stu-id="4074f-124">Default value is 80.</span></span>

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

### <span data-ttu-id="4074f-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="4074f-125">-HttpsPort</span></span>
<span data-ttu-id="4074f-126">Numero di porta TCP HTTPS.</span><span class="sxs-lookup"><span data-stu-id="4074f-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="4074f-127">Deve essere compreso tra 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="4074f-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="4074f-128">Il valore predefinito è 443</span><span class="sxs-lookup"><span data-stu-id="4074f-128">Default value is 443</span></span>

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

### <span data-ttu-id="4074f-129">-Priority</span><span class="sxs-lookup"><span data-stu-id="4074f-129">-Priority</span></span>
<span data-ttu-id="4074f-130">Priorità da usare per il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="4074f-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="4074f-131">Deve essere compreso tra 1 e 5.</span><span class="sxs-lookup"><span data-stu-id="4074f-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="4074f-132">Il valore predefinito è 1</span><span class="sxs-lookup"><span data-stu-id="4074f-132">Default value is 1</span></span>

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

### <span data-ttu-id="4074f-133">-PrivateLinkAlias</span><span class="sxs-lookup"><span data-stu-id="4074f-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="4074f-134">Alias della risorsa Collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="4074f-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="4074f-135">La compilazione di questo campo facoltativo indica che il back-end è 'Privato'</span><span class="sxs-lookup"><span data-stu-id="4074f-135">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="4074f-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="4074f-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="4074f-137">Messaggio personalizzato da includere nella richiesta di approvazione per la connessione al collegamento privato</span><span class="sxs-lookup"><span data-stu-id="4074f-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

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

### <span data-ttu-id="4074f-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="4074f-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="4074f-139">Posizione della risorsa Collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="4074f-139">The Location of Private Link resource.</span></span> <span data-ttu-id="4074f-140">Location è obbligatorio quando PrivateLinkResourceId è impostato</span><span class="sxs-lookup"><span data-stu-id="4074f-140">Location is required when PrivateLinkResourceId is set</span></span>

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

### <span data-ttu-id="4074f-141">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="4074f-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="4074f-142">ID risorsa del collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="4074f-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="4074f-143">La compilazione di questo campo facoltativo indica che il back-end è 'Privato'</span><span class="sxs-lookup"><span data-stu-id="4074f-143">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="4074f-144">-Spessore</span><span class="sxs-lookup"><span data-stu-id="4074f-144">-Weight</span></span>
<span data-ttu-id="4074f-145">Peso di questo endpoint a scopo di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="4074f-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="4074f-146">Deve essere compreso tra 1 e 1000.</span><span class="sxs-lookup"><span data-stu-id="4074f-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="4074f-147">Il valore predefinito è 50</span><span class="sxs-lookup"><span data-stu-id="4074f-147">Default value is 50</span></span>

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

### <span data-ttu-id="4074f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4074f-148">CommonParameters</span></span>
<span data-ttu-id="4074f-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4074f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4074f-150">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4074f-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4074f-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="4074f-151">INPUTS</span></span>

### <span data-ttu-id="4074f-152">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4074f-152">None</span></span>

## <span data-ttu-id="4074f-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4074f-153">OUTPUTS</span></span>

### <span data-ttu-id="4074f-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span><span class="sxs-lookup"><span data-stu-id="4074f-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="4074f-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="4074f-155">NOTES</span></span>

## <span data-ttu-id="4074f-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4074f-156">RELATED LINKS</span></span>

[<span data-ttu-id="4074f-157">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="4074f-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
