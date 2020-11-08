---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 8eee112840fa7d7af81838927017b38988c9649b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191537"
---
# <span data-ttu-id="bb08c-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="bb08c-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="bb08c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb08c-102">SYNOPSIS</span></span>
<span data-ttu-id="bb08c-103">Creare un oggetto PSBackend</span><span class="sxs-lookup"><span data-stu-id="bb08c-103">Create a PSBackend object</span></span>

## <span data-ttu-id="bb08c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb08c-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb08c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb08c-105">DESCRIPTION</span></span>
<span data-ttu-id="bb08c-106">Creare un oggetto PSBackend per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="bb08c-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="bb08c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb08c-107">EXAMPLES</span></span>

### <span data-ttu-id="bb08c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bb08c-108">Example 1</span></span>
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

<span data-ttu-id="bb08c-109">Creare un oggetto PSBackend per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="bb08c-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="bb08c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb08c-110">PARAMETERS</span></span>

### <span data-ttu-id="bb08c-111">-Address</span><span class="sxs-lookup"><span data-stu-id="bb08c-111">-Address</span></span>
<span data-ttu-id="bb08c-112">Posizione del backend (indirizzo IP o FQDN)</span><span class="sxs-lookup"><span data-stu-id="bb08c-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="bb08c-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="bb08c-113">-BackendHostHeader</span></span>
<span data-ttu-id="bb08c-114">Il valore da usare come intestazione host inviata al backend.</span><span class="sxs-lookup"><span data-stu-id="bb08c-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="bb08c-115">Il valore predefinito è l'indirizzo del backend.</span><span class="sxs-lookup"><span data-stu-id="bb08c-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="bb08c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb08c-116">-DefaultProfile</span></span>
<span data-ttu-id="bb08c-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb08c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb08c-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="bb08c-118">-EnabledState</span></span>
<span data-ttu-id="bb08c-119">Se abilitare l'uso di questo backend.</span><span class="sxs-lookup"><span data-stu-id="bb08c-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="bb08c-120">Il valore predefinito è abilitato</span><span class="sxs-lookup"><span data-stu-id="bb08c-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="bb08c-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="bb08c-121">-HttpPort</span></span>
<span data-ttu-id="bb08c-122">Il numero di porta TCP HTTP.</span><span class="sxs-lookup"><span data-stu-id="bb08c-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="bb08c-123">Deve essere compreso tra 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="bb08c-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="bb08c-124">Il valore predefinito è 80.</span><span class="sxs-lookup"><span data-stu-id="bb08c-124">Default value is 80.</span></span>

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

### <span data-ttu-id="bb08c-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="bb08c-125">-HttpsPort</span></span>
<span data-ttu-id="bb08c-126">Numero di porta TCP HTTPS.</span><span class="sxs-lookup"><span data-stu-id="bb08c-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="bb08c-127">Deve essere compreso tra 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="bb08c-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="bb08c-128">Il valore predefinito è 443</span><span class="sxs-lookup"><span data-stu-id="bb08c-128">Default value is 443</span></span>

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

### <span data-ttu-id="bb08c-129">-Priorità</span><span class="sxs-lookup"><span data-stu-id="bb08c-129">-Priority</span></span>
<span data-ttu-id="bb08c-130">Priorità da usare per il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="bb08c-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="bb08c-131">Deve essere compreso tra 1 e 5.</span><span class="sxs-lookup"><span data-stu-id="bb08c-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="bb08c-132">Il valore predefinito è 1</span><span class="sxs-lookup"><span data-stu-id="bb08c-132">Default value is 1</span></span>

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

### <span data-ttu-id="bb08c-133">-PrivateLinkAlias</span><span class="sxs-lookup"><span data-stu-id="bb08c-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="bb08c-134">L'alias della risorsa collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="bb08c-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="bb08c-135">La compilazione di questo campo facoltativo indica che il backend è "privato"</span><span class="sxs-lookup"><span data-stu-id="bb08c-135">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="bb08c-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="bb08c-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="bb08c-137">Messaggio personalizzato da includere nella richiesta di approvazione per la connessione al collegamento privato</span><span class="sxs-lookup"><span data-stu-id="bb08c-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

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

### <span data-ttu-id="bb08c-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="bb08c-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="bb08c-139">Posizione della risorsa collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="bb08c-139">The Location of Private Link resource.</span></span> <span data-ttu-id="bb08c-140">La posizione è obbligatoria quando PrivateLinkResourceId è impostato</span><span class="sxs-lookup"><span data-stu-id="bb08c-140">Location is required when PrivateLinkResourceId is set</span></span>

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

### <span data-ttu-id="bb08c-141">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="bb08c-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="bb08c-142">ID risorsa del collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="bb08c-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="bb08c-143">La compilazione di questo campo facoltativo indica che il backend è "privato"</span><span class="sxs-lookup"><span data-stu-id="bb08c-143">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="bb08c-144">-Peso</span><span class="sxs-lookup"><span data-stu-id="bb08c-144">-Weight</span></span>
<span data-ttu-id="bb08c-145">Peso di questo endpoint per scopi di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="bb08c-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="bb08c-146">Deve essere compreso tra 1 e 1000.</span><span class="sxs-lookup"><span data-stu-id="bb08c-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="bb08c-147">Il valore predefinito è 50</span><span class="sxs-lookup"><span data-stu-id="bb08c-147">Default value is 50</span></span>

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

### <span data-ttu-id="bb08c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb08c-148">CommonParameters</span></span>
<span data-ttu-id="bb08c-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb08c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb08c-150">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb08c-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb08c-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb08c-151">INPUTS</span></span>

### <span data-ttu-id="bb08c-152">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bb08c-152">None</span></span>

## <span data-ttu-id="bb08c-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb08c-153">OUTPUTS</span></span>

### <span data-ttu-id="bb08c-154">Microsoft. Azure. Commands. FrontDoor. Models. PSBackend</span><span class="sxs-lookup"><span data-stu-id="bb08c-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="bb08c-155">Note</span><span class="sxs-lookup"><span data-stu-id="bb08c-155">NOTES</span></span>

## <span data-ttu-id="bb08c-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb08c-156">RELATED LINKS</span></span>

[<span data-ttu-id="bb08c-157">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="bb08c-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
