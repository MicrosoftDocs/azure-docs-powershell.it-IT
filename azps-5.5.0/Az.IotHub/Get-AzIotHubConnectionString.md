---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: f84d233280bc771b90f47c5769fdb6d3f35c2e0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194311"
---
# <span data-ttu-id="d6df9-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="d6df9-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="d6df9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6df9-102">SYNOPSIS</span></span>
<span data-ttu-id="d6df9-103">Ottiene le stringhe di connessione IotHub.</span><span class="sxs-lookup"><span data-stu-id="d6df9-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="d6df9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6df9-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6df9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d6df9-105">DESCRIPTION</span></span>
<span data-ttu-id="d6df9-106">Ottiene le stringhe di connessione IotHub.</span><span class="sxs-lookup"><span data-stu-id="d6df9-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="d6df9-107">È possibile ottenere le stringhe di connessione per tutte le chiavi o filtrarle in base a un nome di chiave specifico.</span><span class="sxs-lookup"><span data-stu-id="d6df9-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="d6df9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6df9-108">EXAMPLES</span></span>

### <span data-ttu-id="d6df9-109">Esempio 1: Recuperare tutte le stringhe di connessione iotHub</span><span class="sxs-lookup"><span data-stu-id="d6df9-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="d6df9-110">Ottiene le stringhe di connessione per tutte le chiavi per il dispositivo iothub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="d6df9-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="d6df9-111">Esempio 2 Ottenere le stringhe di connessione IotHub per una chiave specifica</span><span class="sxs-lookup"><span data-stu-id="d6df9-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="d6df9-112">Ottiene le stringhe di connessione per la chiave denominata "mykey" per il dispositivo iothub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="d6df9-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="d6df9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6df9-113">PARAMETERS</span></span>

### <span data-ttu-id="d6df9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6df9-114">-DefaultProfile</span></span>
<span data-ttu-id="d6df9-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="d6df9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6df9-116">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d6df9-116">-KeyName</span></span>
<span data-ttu-id="d6df9-117">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="d6df9-117">Name of the Key</span></span>

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

### <span data-ttu-id="d6df9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d6df9-118">-Name</span></span>
<span data-ttu-id="d6df9-119">Nome del file IotHub</span><span class="sxs-lookup"><span data-stu-id="d6df9-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="d6df9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6df9-120">-ResourceGroupName</span></span>
<span data-ttu-id="d6df9-121">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d6df9-121">Resource Group Name</span></span>

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

### <span data-ttu-id="d6df9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6df9-122">CommonParameters</span></span>
<span data-ttu-id="d6df9-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6df9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6df9-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6df9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6df9-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="d6df9-125">INPUTS</span></span>

### <span data-ttu-id="d6df9-126">System.String</span><span class="sxs-lookup"><span data-stu-id="d6df9-126">System.String</span></span>

## <span data-ttu-id="d6df9-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6df9-127">OUTPUTS</span></span>

### <span data-ttu-id="d6df9-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d6df9-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="d6df9-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="d6df9-129">NOTES</span></span>

## <span data-ttu-id="d6df9-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6df9-130">RELATED LINKS</span></span>
