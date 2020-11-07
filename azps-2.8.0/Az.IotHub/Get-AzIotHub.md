---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: d544de6badaa6ce64e8165696cc7dff2a595d75e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674245"
---
# <span data-ttu-id="a0802-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="a0802-101">Get-AzIotHub</span></span>

## <span data-ttu-id="a0802-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0802-102">SYNOPSIS</span></span>
<span data-ttu-id="a0802-103">Ottiene le informazioni sul IotHubs in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a0802-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="a0802-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0802-104">SYNTAX</span></span>

### <span data-ttu-id="a0802-105">ListIotHubsByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a0802-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0802-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="a0802-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0802-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0802-107">DESCRIPTION</span></span>
<span data-ttu-id="a0802-108">Ottiene le informazioni sul IotHubs in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a0802-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="a0802-109">Puoi visualizzare tutte le istanze di IotHub in un abbonamento o filtrare i risultati in base a un gruppo di risorse o a un determinato nome di IotHub.</span><span class="sxs-lookup"><span data-stu-id="a0802-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="a0802-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0802-110">EXAMPLES</span></span>

### <span data-ttu-id="a0802-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a0802-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="a0802-112">Ottiene tutti i IotHubs nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a0802-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="a0802-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a0802-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="a0802-114">Ottiene tutti i IotHubs dell'abbonamento appartenenti alla ResourceGroup denominata "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="a0802-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="a0802-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a0802-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="a0802-116">Ottiene informazioni sulla IotHub denominata "myiothub".</span><span class="sxs-lookup"><span data-stu-id="a0802-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="a0802-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0802-117">PARAMETERS</span></span>

### <span data-ttu-id="a0802-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0802-118">-DefaultProfile</span></span>
<span data-ttu-id="a0802-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a0802-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0802-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0802-120">-Name</span></span>
<span data-ttu-id="a0802-121">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="a0802-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="a0802-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0802-122">-ResourceGroupName</span></span>
<span data-ttu-id="a0802-123">Nome del ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a0802-123">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="a0802-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0802-124">CommonParameters</span></span>
<span data-ttu-id="a0802-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0802-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0802-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0802-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0802-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0802-127">INPUTS</span></span>

### <span data-ttu-id="a0802-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a0802-128">System.String</span></span>

## <span data-ttu-id="a0802-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0802-129">OUTPUTS</span></span>

### <span data-ttu-id="a0802-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a0802-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="a0802-131">Note</span><span class="sxs-lookup"><span data-stu-id="a0802-131">NOTES</span></span>

## <span data-ttu-id="a0802-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0802-132">RELATED LINKS</span></span>