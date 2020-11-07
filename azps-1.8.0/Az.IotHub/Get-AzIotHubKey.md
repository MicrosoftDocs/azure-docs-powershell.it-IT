---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: ac56d5392025a85d0310862a1786dde3d0f8ca2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835891"
---
# <span data-ttu-id="7abda-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="7abda-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="7abda-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7abda-102">SYNOPSIS</span></span>
<span data-ttu-id="7abda-103">Ottiene una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="7abda-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="7abda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7abda-104">SYNTAX</span></span>

```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7abda-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7abda-105">DESCRIPTION</span></span>
<span data-ttu-id="7abda-106">Ottiene una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="7abda-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="7abda-107">È possibile elencare tutte le chiavi o filtrare l'elenco in base a un nome di chiave specifico.</span><span class="sxs-lookup"><span data-stu-id="7abda-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="7abda-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7abda-108">EXAMPLES</span></span>

### <span data-ttu-id="7abda-109">Esempio 1 ottenere tutte le chiavi</span><span class="sxs-lookup"><span data-stu-id="7abda-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="7abda-110">Ottiene tutte le chiavi per la IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="7abda-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="7abda-111">Esempio 2 ottenere informazioni per un tasto specifico</span><span class="sxs-lookup"><span data-stu-id="7abda-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="7abda-112">Ottiene le informazioni per una chiave denominata "iothubowner" per la IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="7abda-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="7abda-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7abda-113">PARAMETERS</span></span>

### <span data-ttu-id="7abda-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7abda-114">-DefaultProfile</span></span>
<span data-ttu-id="7abda-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7abda-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7abda-116">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="7abda-116">-KeyName</span></span>
<span data-ttu-id="7abda-117">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="7abda-117">Name of the Key</span></span>

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

### <span data-ttu-id="7abda-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="7abda-118">-Name</span></span>
<span data-ttu-id="7abda-119">Nome dell'hub molto.</span><span class="sxs-lookup"><span data-stu-id="7abda-119">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="7abda-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7abda-120">-ResourceGroupName</span></span>
<span data-ttu-id="7abda-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="7abda-121">Resource Group Name</span></span>

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

### <span data-ttu-id="7abda-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7abda-122">CommonParameters</span></span>
<span data-ttu-id="7abda-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7abda-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7abda-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7abda-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7abda-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7abda-125">INPUTS</span></span>

### <span data-ttu-id="7abda-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7abda-126">System.String</span></span>

## <span data-ttu-id="7abda-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7abda-127">OUTPUTS</span></span>

### <span data-ttu-id="7abda-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7abda-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="7abda-129">Note</span><span class="sxs-lookup"><span data-stu-id="7abda-129">NOTES</span></span>

## <span data-ttu-id="7abda-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7abda-130">RELATED LINKS</span></span>
