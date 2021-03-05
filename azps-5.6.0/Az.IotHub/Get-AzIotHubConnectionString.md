---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: ba5ab4214de0272338bac61cdf1bbabc9507a9ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988117"
---
# <span data-ttu-id="2b065-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="2b065-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="2b065-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b065-102">SYNOPSIS</span></span>
<span data-ttu-id="2b065-103">Ottiene le stringhe di connessione IotHub.</span><span class="sxs-lookup"><span data-stu-id="2b065-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="2b065-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b065-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b065-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2b065-105">DESCRIPTION</span></span>
<span data-ttu-id="2b065-106">Ottiene le stringhe di connessione IotHub.</span><span class="sxs-lookup"><span data-stu-id="2b065-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="2b065-107">È possibile ottenere le stringhe di connessione per tutte le chiavi o filtrarle in base a un nome di chiave specifico.</span><span class="sxs-lookup"><span data-stu-id="2b065-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="2b065-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b065-108">EXAMPLES</span></span>

### <span data-ttu-id="2b065-109">Esempio 1: Recuperare tutte le stringhe di connessione iotHub</span><span class="sxs-lookup"><span data-stu-id="2b065-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="2b065-110">Ottiene le stringhe di connessione per tutte le chiavi per il dispositivo iothub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="2b065-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="2b065-111">Esempio 2 Ottenere le stringhe di connessione IotHub per una chiave specifica</span><span class="sxs-lookup"><span data-stu-id="2b065-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="2b065-112">Ottiene le stringhe di connessione per la chiave denominata "mykey" per il dispositivo iothub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="2b065-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="2b065-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b065-113">PARAMETERS</span></span>

### <span data-ttu-id="2b065-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b065-114">-DefaultProfile</span></span>
<span data-ttu-id="2b065-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2b065-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b065-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="2b065-116">-KeyName</span></span>
<span data-ttu-id="2b065-117">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="2b065-117">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b065-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2b065-118">-Name</span></span>
<span data-ttu-id="2b065-119">Nome del file IotHub</span><span class="sxs-lookup"><span data-stu-id="2b065-119">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b065-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b065-120">-ResourceGroupName</span></span>
<span data-ttu-id="2b065-121">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2b065-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b065-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b065-122">CommonParameters</span></span>
<span data-ttu-id="2b065-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b065-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b065-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b065-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b065-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="2b065-125">INPUTS</span></span>

### <span data-ttu-id="2b065-126">System.String</span><span class="sxs-lookup"><span data-stu-id="2b065-126">System.String</span></span>

## <span data-ttu-id="2b065-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b065-127">OUTPUTS</span></span>

### <span data-ttu-id="2b065-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2b065-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="2b065-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="2b065-129">NOTES</span></span>

## <span data-ttu-id="2b065-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b065-130">RELATED LINKS</span></span>
