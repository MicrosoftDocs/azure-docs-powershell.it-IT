---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
ms.openlocfilehash: db2cf6c9daae5b96642a6408b990276feffc8598
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520076"
---
# <span data-ttu-id="ffecc-101">Get-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="ffecc-101">Get-AzureRmIotHubKey</span></span>

## <span data-ttu-id="ffecc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ffecc-102">SYNOPSIS</span></span>
<span data-ttu-id="ffecc-103">Ottiene una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="ffecc-103">Gets an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffecc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ffecc-104">SYNTAX</span></span>

```
Get-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffecc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ffecc-105">DESCRIPTION</span></span>
<span data-ttu-id="ffecc-106">Ottiene una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="ffecc-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="ffecc-107">È possibile elencare tutte le chiavi o filtrare l'elenco in base a un nome di chiave specifico.</span><span class="sxs-lookup"><span data-stu-id="ffecc-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="ffecc-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ffecc-108">EXAMPLES</span></span>

### <span data-ttu-id="ffecc-109">Esempio 1 ottenere tutte le chiavi</span><span class="sxs-lookup"><span data-stu-id="ffecc-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="ffecc-110">Ottiene tutte le chiavi per la IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="ffecc-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="ffecc-111">Esempio 2 ottenere informazioni per un tasto specifico</span><span class="sxs-lookup"><span data-stu-id="ffecc-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="ffecc-112">Ottiene le informazioni per una chiave denominata "iothubowner" per la IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="ffecc-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="ffecc-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ffecc-113">PARAMETERS</span></span>

### <span data-ttu-id="ffecc-114">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="ffecc-114">-KeyName</span></span>
<span data-ttu-id="ffecc-115">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="ffecc-115">Name of the Key</span></span>

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

### <span data-ttu-id="ffecc-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="ffecc-116">-Name</span></span>
<span data-ttu-id="ffecc-117">Nome dell'hub molto.</span><span class="sxs-lookup"><span data-stu-id="ffecc-117">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="ffecc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffecc-118">-ResourceGroupName</span></span>
<span data-ttu-id="ffecc-119">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ffecc-119">Resource Group Name</span></span>

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

### <span data-ttu-id="ffecc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffecc-120">-DefaultProfile</span></span>
<span data-ttu-id="ffecc-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ffecc-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffecc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffecc-122">CommonParameters</span></span>
<span data-ttu-id="ffecc-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffecc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffecc-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffecc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffecc-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ffecc-125">INPUTS</span></span>

### <span data-ttu-id="ffecc-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ffecc-126">System.String</span></span>

## <span data-ttu-id="ffecc-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ffecc-127">OUTPUTS</span></span>

### <span data-ttu-id="ffecc-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ffecc-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="ffecc-129">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="ffecc-129">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="ffecc-130">Note</span><span class="sxs-lookup"><span data-stu-id="ffecc-130">NOTES</span></span>

## <span data-ttu-id="ffecc-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ffecc-131">RELATED LINKS</span></span>

