---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: 92d1e3f2ef1ba87a5e9683f7ac6617e31bb8a055
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861397"
---
# <span data-ttu-id="52280-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="52280-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="52280-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52280-102">SYNOPSIS</span></span>
<span data-ttu-id="52280-103">Ottiene il IotHub connectionStrings.</span><span class="sxs-lookup"><span data-stu-id="52280-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="52280-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52280-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52280-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52280-105">DESCRIPTION</span></span>
<span data-ttu-id="52280-106">Ottiene il IotHub connectionStrings.</span><span class="sxs-lookup"><span data-stu-id="52280-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="52280-107">È possibile ottenere connectionStrings per tutte le chiavi oppure filtrarle con un nome di chiave specifico.</span><span class="sxs-lookup"><span data-stu-id="52280-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="52280-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52280-108">EXAMPLES</span></span>

### <span data-ttu-id="52280-109">Esempio 1 ottenere tutte le IotHub connectionStrings</span><span class="sxs-lookup"><span data-stu-id="52280-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="52280-110">Ottiene la connectionStrings per tutte le chiavi per iothub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="52280-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="52280-111">Esempio 2 ottenere la IotHub connectionStrings per una chiave specifica</span><span class="sxs-lookup"><span data-stu-id="52280-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="52280-112">Ottiene i connectionStrings per la chiave denominata "myKey" per la iothub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="52280-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="52280-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52280-113">PARAMETERS</span></span>

### <span data-ttu-id="52280-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52280-114">-DefaultProfile</span></span>
<span data-ttu-id="52280-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="52280-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52280-116">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="52280-116">-KeyName</span></span>
<span data-ttu-id="52280-117">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="52280-117">Name of the Key</span></span>

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

### <span data-ttu-id="52280-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="52280-118">-Name</span></span>
<span data-ttu-id="52280-119">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="52280-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="52280-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52280-120">-ResourceGroupName</span></span>
<span data-ttu-id="52280-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="52280-121">Resource Group Name</span></span>

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

### <span data-ttu-id="52280-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52280-122">CommonParameters</span></span>
<span data-ttu-id="52280-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52280-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52280-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52280-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52280-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52280-125">INPUTS</span></span>

### <span data-ttu-id="52280-126">System. String</span><span class="sxs-lookup"><span data-stu-id="52280-126">System.String</span></span>

## <span data-ttu-id="52280-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52280-127">OUTPUTS</span></span>

### <span data-ttu-id="52280-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="52280-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="52280-129">Note</span><span class="sxs-lookup"><span data-stu-id="52280-129">NOTES</span></span>

## <span data-ttu-id="52280-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52280-130">RELATED LINKS</span></span>
