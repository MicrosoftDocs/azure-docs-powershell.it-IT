---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendObject.md
ms.openlocfilehash: 429db1fae2987531911bd4dfbd4c41daf66a5440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686395"
---
# <span data-ttu-id="e7f0c-101">New-AzureRmFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="e7f0c-101">New-AzureRmFrontDoorBackendObject</span></span>

## <span data-ttu-id="e7f0c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e7f0c-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f0c-103">Creare un oggetto PSBackend</span><span class="sxs-lookup"><span data-stu-id="e7f0c-103">Create a PSBackend object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7f0c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7f0c-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-Priority <Int32>] [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7f0c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7f0c-105">DESCRIPTION</span></span>
<span data-ttu-id="e7f0c-106">Creare un oggetto PSBackend per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="e7f0c-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="e7f0c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7f0c-107">EXAMPLES</span></span>

### <span data-ttu-id="e7f0c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e7f0c-108">Example 1</span></span>
```powershell
PS C:\>New-AzureRmFrontDoorBackendObject -Address "contoso1.azurewebsites.net"


Address           : contoso1.azurewebsites.net
HttpPort          : 80
HttpsPort         : 443
Priority          : 1
Weight            : 50
BackendHostHeader :
EnabledState      : Enabled
```

<span data-ttu-id="e7f0c-109">Creare un oggetto PSBackend per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="e7f0c-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="e7f0c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e7f0c-110">PARAMETERS</span></span>

### <span data-ttu-id="e7f0c-111">-Address</span><span class="sxs-lookup"><span data-stu-id="e7f0c-111">-Address</span></span>
<span data-ttu-id="e7f0c-112">Posizione del backend (indirizzo IP o FQDN)</span><span class="sxs-lookup"><span data-stu-id="e7f0c-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="e7f0c-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="e7f0c-113">-BackendHostHeader</span></span>
<span data-ttu-id="e7f0c-114">Il valore da usare come intestazione host inviata al backend.</span><span class="sxs-lookup"><span data-stu-id="e7f0c-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="e7f0c-115">Il valore predefinito è l'indirizzo del backend.</span><span class="sxs-lookup"><span data-stu-id="e7f0c-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="e7f0c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f0c-116">-DefaultProfile</span></span>
<span data-ttu-id="e7f0c-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e7f0c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7f0c-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="e7f0c-118">-EnabledState</span></span>
<span data-ttu-id="e7f0c-119">Se abilitare l'uso di questo backend.</span><span class="sxs-lookup"><span data-stu-id="e7f0c-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="e7f0c-120">Il valore predefinito è abilitato</span><span class="sxs-lookup"><span data-stu-id="e7f0c-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="e7f0c-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="e7f0c-121">-HttpPort</span></span>
<span data-ttu-id="e7f0c-122">Il numero di porta TCP HTTP.</span><span class="sxs-lookup"><span data-stu-id="e7f0c-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="e7f0c-123">Deve essere compreso tra 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="e7f0c-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="e7f0c-124">Il valore predefinito è 80.</span><span class="sxs-lookup"><span data-stu-id="e7f0c-124">Default value is 80.</span></span>

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

### <span data-ttu-id="e7f0c-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="e7f0c-125">-HttpsPort</span></span>
<span data-ttu-id="e7f0c-126">Numero di porta TCP HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e7f0c-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="e7f0c-127">Deve essere compreso tra 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="e7f0c-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="e7f0c-128">Il valore predefinito è 443</span><span class="sxs-lookup"><span data-stu-id="e7f0c-128">Default value is 443</span></span>

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

### <span data-ttu-id="e7f0c-129">-Priorità</span><span class="sxs-lookup"><span data-stu-id="e7f0c-129">-Priority</span></span>
<span data-ttu-id="e7f0c-130">Priorità da usare per il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e7f0c-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="e7f0c-131">Deve essere compreso tra 1 e 5.</span><span class="sxs-lookup"><span data-stu-id="e7f0c-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="e7f0c-132">Il valore predefinito è 1</span><span class="sxs-lookup"><span data-stu-id="e7f0c-132">Default value is 1</span></span>

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

### <span data-ttu-id="e7f0c-133">-Peso</span><span class="sxs-lookup"><span data-stu-id="e7f0c-133">-Weight</span></span>
<span data-ttu-id="e7f0c-134">Peso di questo endpoint per scopi di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e7f0c-134">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="e7f0c-135">Deve essere compreso tra 1 e 1000.</span><span class="sxs-lookup"><span data-stu-id="e7f0c-135">Must be between 1 and 1000.</span></span>
<span data-ttu-id="e7f0c-136">Il valore predefinito è 50</span><span class="sxs-lookup"><span data-stu-id="e7f0c-136">Default value is 50</span></span>

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

### <span data-ttu-id="e7f0c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f0c-137">CommonParameters</span></span>
<span data-ttu-id="e7f0c-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7f0c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f0c-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7f0c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f0c-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e7f0c-140">INPUTS</span></span>

### <span data-ttu-id="e7f0c-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e7f0c-141">None</span></span>

## <span data-ttu-id="e7f0c-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7f0c-142">OUTPUTS</span></span>

### <span data-ttu-id="e7f0c-143">Microsoft. Azure. Commands. FrontDoor. Models. PSBackend</span><span class="sxs-lookup"><span data-stu-id="e7f0c-143">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="e7f0c-144">Note</span><span class="sxs-lookup"><span data-stu-id="e7f0c-144">NOTES</span></span>

## <span data-ttu-id="e7f0c-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7f0c-145">RELATED LINKS</span></span>

[<span data-ttu-id="e7f0c-146">New-AzureRmFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="e7f0c-146">New-AzureRmFrontDoorBackendPoolObject</span></span>](./New-AzureRmFrontDoorBackendPoolObject.md)
