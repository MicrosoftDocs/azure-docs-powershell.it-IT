---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: c38965a99dfc152f76e606c05802009b9b14faf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674234"
---
# <span data-ttu-id="79f8e-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="79f8e-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="79f8e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79f8e-102">SYNOPSIS</span></span>
<span data-ttu-id="79f8e-103">Ottiene una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="79f8e-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="79f8e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79f8e-104">SYNTAX</span></span>

### <span data-ttu-id="79f8e-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="79f8e-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79f8e-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="79f8e-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79f8e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79f8e-107">DESCRIPTION</span></span>
<span data-ttu-id="79f8e-108">Ottiene una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="79f8e-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="79f8e-109">È possibile elencare tutte le chiavi o filtrare l'elenco in base a un nome di chiave specifico.</span><span class="sxs-lookup"><span data-stu-id="79f8e-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="79f8e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79f8e-110">EXAMPLES</span></span>

### <span data-ttu-id="79f8e-111">Esempio 1 ottenere tutte le chiavi</span><span class="sxs-lookup"><span data-stu-id="79f8e-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="79f8e-112">Ottiene tutte le chiavi per la IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="79f8e-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="79f8e-113">Esempio 2 ottenere informazioni per un tasto specifico</span><span class="sxs-lookup"><span data-stu-id="79f8e-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="79f8e-114">Ottiene le informazioni per una chiave denominata "iothubowner" per la IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="79f8e-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="79f8e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79f8e-115">PARAMETERS</span></span>

### <span data-ttu-id="79f8e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79f8e-116">-DefaultProfile</span></span>
<span data-ttu-id="79f8e-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="79f8e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79f8e-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="79f8e-118">-HubId</span></span>
<span data-ttu-id="79f8e-119">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="79f8e-119">IotHub Resource Id</span></span>

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

### <span data-ttu-id="79f8e-120">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="79f8e-120">-KeyName</span></span>
<span data-ttu-id="79f8e-121">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="79f8e-121">Name of the Key</span></span>

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

### <span data-ttu-id="79f8e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="79f8e-122">-Name</span></span>
<span data-ttu-id="79f8e-123">Nome dell'hub molto.</span><span class="sxs-lookup"><span data-stu-id="79f8e-123">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="79f8e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79f8e-124">-ResourceGroupName</span></span>
<span data-ttu-id="79f8e-125">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="79f8e-125">Resource Group Name</span></span>

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

### <span data-ttu-id="79f8e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79f8e-126">CommonParameters</span></span>
<span data-ttu-id="79f8e-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79f8e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79f8e-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79f8e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79f8e-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79f8e-129">INPUTS</span></span>

### <span data-ttu-id="79f8e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="79f8e-130">System.String</span></span>

## <span data-ttu-id="79f8e-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79f8e-131">OUTPUTS</span></span>

### <span data-ttu-id="79f8e-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="79f8e-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="79f8e-133">Note</span><span class="sxs-lookup"><span data-stu-id="79f8e-133">NOTES</span></span>

## <span data-ttu-id="79f8e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79f8e-134">RELATED LINKS</span></span>
