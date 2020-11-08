---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 0656726757584bf923d6ecaa7642aa67ff46596a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192880"
---
# <span data-ttu-id="23a99-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="23a99-101">Get-AzIotHub</span></span>

## <span data-ttu-id="23a99-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="23a99-102">SYNOPSIS</span></span>
<span data-ttu-id="23a99-103">Ottiene le informazioni sul IotHubs in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="23a99-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="23a99-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23a99-104">SYNTAX</span></span>

### <span data-ttu-id="23a99-105">ListIotHubsByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="23a99-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23a99-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="23a99-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23a99-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23a99-107">DESCRIPTION</span></span>
<span data-ttu-id="23a99-108">Ottiene le informazioni sul IotHubs in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="23a99-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="23a99-109">Puoi visualizzare tutte le istanze di IotHub in un abbonamento o filtrare i risultati in base a un gruppo di risorse o a un determinato nome di IotHub.</span><span class="sxs-lookup"><span data-stu-id="23a99-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="23a99-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23a99-110">EXAMPLES</span></span>

### <span data-ttu-id="23a99-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="23a99-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="23a99-112">Ottiene tutti i IotHubs nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="23a99-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="23a99-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="23a99-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="23a99-114">Ottiene tutti i IotHubs dell'abbonamento appartenenti alla ResourceGroup denominata "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="23a99-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="23a99-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="23a99-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="23a99-116">Ottiene informazioni sulla IotHub denominata "myiothub".</span><span class="sxs-lookup"><span data-stu-id="23a99-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="23a99-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="23a99-117">PARAMETERS</span></span>

### <span data-ttu-id="23a99-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23a99-118">-DefaultProfile</span></span>
<span data-ttu-id="23a99-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="23a99-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23a99-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="23a99-120">-Name</span></span>
<span data-ttu-id="23a99-121">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="23a99-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23a99-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23a99-122">-ResourceGroupName</span></span>
<span data-ttu-id="23a99-123">Nome del ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="23a99-123">Name of the ResourceGroup</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotHubsByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23a99-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23a99-124">CommonParameters</span></span>
<span data-ttu-id="23a99-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23a99-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23a99-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23a99-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23a99-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="23a99-127">INPUTS</span></span>

### <span data-ttu-id="23a99-128">System. String</span><span class="sxs-lookup"><span data-stu-id="23a99-128">System.String</span></span>

## <span data-ttu-id="23a99-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23a99-129">OUTPUTS</span></span>

### <span data-ttu-id="23a99-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="23a99-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="23a99-131">Note</span><span class="sxs-lookup"><span data-stu-id="23a99-131">NOTES</span></span>

## <span data-ttu-id="23a99-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23a99-132">RELATED LINKS</span></span>
