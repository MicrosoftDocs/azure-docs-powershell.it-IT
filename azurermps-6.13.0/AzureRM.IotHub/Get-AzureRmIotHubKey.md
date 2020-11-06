---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
ms.openlocfilehash: 33232e5e8f415309bec36f8918c272c251835f82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520994"
---
# <span data-ttu-id="8deae-101">Get-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="8deae-101">Get-AzureRmIotHubKey</span></span>

## <span data-ttu-id="8deae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8deae-102">SYNOPSIS</span></span>
<span data-ttu-id="8deae-103">Ottiene una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="8deae-103">Gets an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8deae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8deae-104">SYNTAX</span></span>

```
Get-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8deae-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8deae-105">DESCRIPTION</span></span>
<span data-ttu-id="8deae-106">Ottiene una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="8deae-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="8deae-107">È possibile elencare tutte le chiavi o filtrare l'elenco in base a un nome di chiave specifico.</span><span class="sxs-lookup"><span data-stu-id="8deae-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="8deae-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8deae-108">EXAMPLES</span></span>

### <span data-ttu-id="8deae-109">Esempio 1 ottenere tutte le chiavi</span><span class="sxs-lookup"><span data-stu-id="8deae-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="8deae-110">Ottiene tutte le chiavi per la IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="8deae-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="8deae-111">Esempio 2 ottenere informazioni per un tasto specifico</span><span class="sxs-lookup"><span data-stu-id="8deae-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="8deae-112">Ottiene le informazioni per una chiave denominata "iothubowner" per la IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="8deae-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="8deae-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8deae-113">PARAMETERS</span></span>

### <span data-ttu-id="8deae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8deae-114">-DefaultProfile</span></span>
<span data-ttu-id="8deae-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8deae-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8deae-116">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="8deae-116">-KeyName</span></span>
<span data-ttu-id="8deae-117">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="8deae-117">Name of the Key</span></span>

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

### <span data-ttu-id="8deae-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="8deae-118">-Name</span></span>
<span data-ttu-id="8deae-119">Nome dell'hub molto.</span><span class="sxs-lookup"><span data-stu-id="8deae-119">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="8deae-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8deae-120">-ResourceGroupName</span></span>
<span data-ttu-id="8deae-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="8deae-121">Resource Group Name</span></span>

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

### <span data-ttu-id="8deae-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8deae-122">CommonParameters</span></span>
<span data-ttu-id="8deae-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8deae-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8deae-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8deae-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8deae-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8deae-125">INPUTS</span></span>

### <span data-ttu-id="8deae-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8deae-126">System.String</span></span>

## <span data-ttu-id="8deae-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8deae-127">OUTPUTS</span></span>

### <span data-ttu-id="8deae-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8deae-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="8deae-129">Note</span><span class="sxs-lookup"><span data-stu-id="8deae-129">NOTES</span></span>

## <span data-ttu-id="8deae-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8deae-130">RELATED LINKS</span></span>
