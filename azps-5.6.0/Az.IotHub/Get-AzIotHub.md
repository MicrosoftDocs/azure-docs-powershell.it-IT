---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 6937d79d6f60c053238075713f5d58432124e7e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988173"
---
# <span data-ttu-id="ab8af-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="ab8af-101">Get-AzIotHub</span></span>

## <span data-ttu-id="ab8af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab8af-102">SYNOPSIS</span></span>
<span data-ttu-id="ab8af-103">Ottiene informazioni sugli IotHub in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ab8af-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="ab8af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab8af-104">SYNTAX</span></span>

### <span data-ttu-id="ab8af-105">ListIotHubsByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ab8af-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab8af-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="ab8af-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab8af-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ab8af-107">DESCRIPTION</span></span>
<span data-ttu-id="ab8af-108">Ottiene informazioni sugli IotHub in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ab8af-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="ab8af-109">È possibile visualizzare tutte le istanze di IotHub in una sottoscrizione oppure filtrare i risultati in base a un gruppo di risorse o a un nome specifico di IotHub.</span><span class="sxs-lookup"><span data-stu-id="ab8af-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="ab8af-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab8af-110">EXAMPLES</span></span>

### <span data-ttu-id="ab8af-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ab8af-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="ab8af-112">Recupera tutti gli IotHub nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ab8af-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="ab8af-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ab8af-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="ab8af-114">Ottiene tutti gli IotHub nella sottoscrizione appartenente al gruppo di risorse denominato "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="ab8af-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="ab8af-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="ab8af-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="ab8af-116">Recupera informazioni sul sito IotHub denominato "myiothub".</span><span class="sxs-lookup"><span data-stu-id="ab8af-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="ab8af-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab8af-117">PARAMETERS</span></span>

### <span data-ttu-id="ab8af-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab8af-118">-DefaultProfile</span></span>
<span data-ttu-id="ab8af-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ab8af-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab8af-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ab8af-120">-Name</span></span>
<span data-ttu-id="ab8af-121">Nome del file IotHub</span><span class="sxs-lookup"><span data-stu-id="ab8af-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="ab8af-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab8af-122">-ResourceGroupName</span></span>
<span data-ttu-id="ab8af-123">Nome del Gruppo Risorse</span><span class="sxs-lookup"><span data-stu-id="ab8af-123">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="ab8af-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab8af-124">CommonParameters</span></span>
<span data-ttu-id="ab8af-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab8af-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab8af-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab8af-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab8af-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="ab8af-127">INPUTS</span></span>

### <span data-ttu-id="ab8af-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ab8af-128">System.String</span></span>

## <span data-ttu-id="ab8af-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab8af-129">OUTPUTS</span></span>

### <span data-ttu-id="ab8af-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ab8af-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="ab8af-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="ab8af-131">NOTES</span></span>

## <span data-ttu-id="ab8af-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab8af-132">RELATED LINKS</span></span>
