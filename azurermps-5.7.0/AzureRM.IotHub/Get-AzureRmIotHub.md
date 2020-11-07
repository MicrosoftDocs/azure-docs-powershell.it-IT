---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
ms.openlocfilehash: 80b629fe3d5ff5e028b73b22af95243849ecede7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686104"
---
# <span data-ttu-id="6dde0-101">Get-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="6dde0-101">Get-AzureRmIotHub</span></span>

## <span data-ttu-id="6dde0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6dde0-102">SYNOPSIS</span></span>
<span data-ttu-id="6dde0-103">Ottiene le informazioni sul IotHubs in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6dde0-103">Gets information about the IotHubs in a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6dde0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6dde0-104">SYNTAX</span></span>

### <span data-ttu-id="6dde0-105">ListIotHubsByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6dde0-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzureRmIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6dde0-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="6dde0-106">GetIotHubByName</span></span>
```
Get-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6dde0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6dde0-107">DESCRIPTION</span></span>
<span data-ttu-id="6dde0-108">Ottiene le informazioni sul IotHubs in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6dde0-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="6dde0-109">Puoi visualizzare tutte le istanze di IotHub in un abbonamento o filtrare i risultati in base a un gruppo di risorse o a un determinato nome di IotHub.</span><span class="sxs-lookup"><span data-stu-id="6dde0-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="6dde0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6dde0-110">EXAMPLES</span></span>

### <span data-ttu-id="6dde0-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6dde0-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHub
```

<span data-ttu-id="6dde0-112">Ottiene tutti i IotHubs nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6dde0-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="6dde0-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6dde0-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="6dde0-114">Ottiene tutti i IotHubs dell'abbonamento appartenenti alla ResourceGroup denominata "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="6dde0-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="6dde0-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6dde0-115">Example 3</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="6dde0-116">Ottiene informazioni sulla IotHub denominata "myiothub".</span><span class="sxs-lookup"><span data-stu-id="6dde0-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="6dde0-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6dde0-117">PARAMETERS</span></span>

### <span data-ttu-id="6dde0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dde0-118">-DefaultProfile</span></span>
<span data-ttu-id="6dde0-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6dde0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6dde0-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6dde0-120">-Name</span></span>
<span data-ttu-id="6dde0-121">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="6dde0-121">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dde0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dde0-122">-ResourceGroupName</span></span>
<span data-ttu-id="6dde0-123">Nome del ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6dde0-123">Name of the ResourceGroup</span></span>

```yaml
Type: String
Parameter Sets: ListIotHubsByResourceGroup
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dde0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dde0-124">CommonParameters</span></span>
<span data-ttu-id="6dde0-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dde0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dde0-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dde0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dde0-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6dde0-127">INPUTS</span></span>

### <span data-ttu-id="6dde0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6dde0-128">System.String</span></span>

## <span data-ttu-id="6dde0-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6dde0-129">OUTPUTS</span></span>

### <span data-ttu-id="6dde0-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6dde0-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="6dde0-131">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="6dde0-131">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="6dde0-132">Note</span><span class="sxs-lookup"><span data-stu-id="6dde0-132">NOTES</span></span>

## <span data-ttu-id="6dde0-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6dde0-133">RELATED LINKS</span></span>

