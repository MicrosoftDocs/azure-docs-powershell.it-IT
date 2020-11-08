---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 258d1e1bad9eca1fd8817e1eaa499eb5bc3d8d49
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192879"
---
# <span data-ttu-id="ce4ad-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="ce4ad-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="ce4ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce4ad-102">SYNOPSIS</span></span>
<span data-ttu-id="ce4ad-103">Ottiene una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="ce4ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce4ad-104">SYNTAX</span></span>

### <span data-ttu-id="ce4ad-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ce4ad-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce4ad-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ce4ad-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce4ad-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce4ad-107">DESCRIPTION</span></span>
<span data-ttu-id="ce4ad-108">Ottiene una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="ce4ad-109">È possibile elencare tutte le chiavi o filtrare l'elenco in base a un nome di chiave specifico.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="ce4ad-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce4ad-110">EXAMPLES</span></span>

### <span data-ttu-id="ce4ad-111">Esempio 1 ottenere tutte le chiavi</span><span class="sxs-lookup"><span data-stu-id="ce4ad-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="ce4ad-112">Ottiene tutte le chiavi per la IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="ce4ad-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="ce4ad-113">Esempio 2 ottenere informazioni per un tasto specifico</span><span class="sxs-lookup"><span data-stu-id="ce4ad-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="ce4ad-114">Ottiene le informazioni per una chiave denominata "iothubowner" per la IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="ce4ad-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="ce4ad-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce4ad-115">PARAMETERS</span></span>

### <span data-ttu-id="ce4ad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce4ad-116">-DefaultProfile</span></span>
<span data-ttu-id="ce4ad-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ce4ad-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce4ad-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="ce4ad-118">-HubId</span></span>
<span data-ttu-id="ce4ad-119">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="ce4ad-119">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce4ad-120">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="ce4ad-120">-KeyName</span></span>
<span data-ttu-id="ce4ad-121">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="ce4ad-121">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce4ad-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce4ad-122">-Name</span></span>
<span data-ttu-id="ce4ad-123">Nome dell'hub molto.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-123">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce4ad-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce4ad-124">-ResourceGroupName</span></span>
<span data-ttu-id="ce4ad-125">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ce4ad-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce4ad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce4ad-126">CommonParameters</span></span>
<span data-ttu-id="ce4ad-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce4ad-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce4ad-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce4ad-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce4ad-129">INPUTS</span></span>

### <span data-ttu-id="ce4ad-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ce4ad-130">System.String</span></span>

## <span data-ttu-id="ce4ad-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce4ad-131">OUTPUTS</span></span>

### <span data-ttu-id="ce4ad-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ce4ad-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="ce4ad-133">Note</span><span class="sxs-lookup"><span data-stu-id="ce4ad-133">NOTES</span></span>

## <span data-ttu-id="ce4ad-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce4ad-134">RELATED LINKS</span></span>
