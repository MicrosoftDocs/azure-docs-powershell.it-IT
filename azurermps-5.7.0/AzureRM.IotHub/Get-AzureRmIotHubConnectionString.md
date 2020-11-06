---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
ms.openlocfilehash: ef4ac5058c1ce85e19a9854bcd11fc2fac5ac69e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515684"
---
# <span data-ttu-id="90474-101">Get-AzureRmIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="90474-101">Get-AzureRmIotHubConnectionString</span></span>

## <span data-ttu-id="90474-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="90474-102">SYNOPSIS</span></span>
<span data-ttu-id="90474-103">Ottiene il IotHub connectionStrings.</span><span class="sxs-lookup"><span data-stu-id="90474-103">Gets the IotHub connectionstrings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90474-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90474-104">SYNTAX</span></span>

```
Get-AzureRmIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90474-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90474-105">DESCRIPTION</span></span>
<span data-ttu-id="90474-106">Ottiene il IotHub connectionStrings.</span><span class="sxs-lookup"><span data-stu-id="90474-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="90474-107">È possibile ottenere connectionStrings per tutte le chiavi oppure filtrarle con un nome di chiave specifico.</span><span class="sxs-lookup"><span data-stu-id="90474-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="90474-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90474-108">EXAMPLES</span></span>

### <span data-ttu-id="90474-109">Esempio 1 ottenere tutte le IotHub connectionStrings</span><span class="sxs-lookup"><span data-stu-id="90474-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="90474-110">Ottiene la connectionStrings per tutte le chiavi per iothub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="90474-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="90474-111">Esempio 2 ottenere la IotHub connectionStrings per una chiave specifica</span><span class="sxs-lookup"><span data-stu-id="90474-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="90474-112">Ottiene i connectionStrings per la chiave denominata "myKey" per la iothub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="90474-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="90474-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="90474-113">PARAMETERS</span></span>

### <span data-ttu-id="90474-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90474-114">-DefaultProfile</span></span>
<span data-ttu-id="90474-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="90474-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90474-116">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="90474-116">-KeyName</span></span>
<span data-ttu-id="90474-117">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="90474-117">Name of the Key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90474-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="90474-118">-Name</span></span>
<span data-ttu-id="90474-119">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="90474-119">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90474-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90474-120">-ResourceGroupName</span></span>
<span data-ttu-id="90474-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="90474-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90474-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90474-122">CommonParameters</span></span>
<span data-ttu-id="90474-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90474-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90474-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90474-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90474-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="90474-125">INPUTS</span></span>

### <span data-ttu-id="90474-126">System. String</span><span class="sxs-lookup"><span data-stu-id="90474-126">System.String</span></span>

## <span data-ttu-id="90474-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90474-127">OUTPUTS</span></span>

### <span data-ttu-id="90474-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="90474-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="90474-129">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="90474-129">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="90474-130">Note</span><span class="sxs-lookup"><span data-stu-id="90474-130">NOTES</span></span>

## <span data-ttu-id="90474-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90474-131">RELATED LINKS</span></span>

