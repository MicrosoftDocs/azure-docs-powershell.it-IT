---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 0656726757584bf923d6ecaa7642aa67ff46596a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192439"
---
# <span data-ttu-id="d663a-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="d663a-101">Get-AzIotHub</span></span>

## <span data-ttu-id="d663a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d663a-102">SYNOPSIS</span></span>
<span data-ttu-id="d663a-103">Ottiene informazioni sugli IotHub in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d663a-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="d663a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d663a-104">SYNTAX</span></span>

### <span data-ttu-id="d663a-105">ListIotHubsByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d663a-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d663a-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="d663a-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d663a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d663a-107">DESCRIPTION</span></span>
<span data-ttu-id="d663a-108">Ottiene informazioni sugli IotHub in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d663a-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="d663a-109">È possibile visualizzare tutte le istanze di IotHub in una sottoscrizione oppure filtrare i risultati in base a un gruppo di risorse o a un nome specifico di IotHub.</span><span class="sxs-lookup"><span data-stu-id="d663a-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="d663a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d663a-110">EXAMPLES</span></span>

### <span data-ttu-id="d663a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d663a-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="d663a-112">Recupera tutti gli IotHub nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d663a-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="d663a-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d663a-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="d663a-114">Ottiene tutti gli IotHub nella sottoscrizione appartenente al gruppo di risorse denominato "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="d663a-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="d663a-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d663a-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="d663a-116">Recupera informazioni sul sito IotHub denominato "myiothub".</span><span class="sxs-lookup"><span data-stu-id="d663a-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="d663a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d663a-117">PARAMETERS</span></span>

### <span data-ttu-id="d663a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d663a-118">-DefaultProfile</span></span>
<span data-ttu-id="d663a-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="d663a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d663a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d663a-120">-Name</span></span>
<span data-ttu-id="d663a-121">Nome del file IotHub</span><span class="sxs-lookup"><span data-stu-id="d663a-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="d663a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d663a-122">-ResourceGroupName</span></span>
<span data-ttu-id="d663a-123">Nome del Gruppo Risorse</span><span class="sxs-lookup"><span data-stu-id="d663a-123">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="d663a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d663a-124">CommonParameters</span></span>
<span data-ttu-id="d663a-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d663a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d663a-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d663a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d663a-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="d663a-127">INPUTS</span></span>

### <span data-ttu-id="d663a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d663a-128">System.String</span></span>

## <span data-ttu-id="d663a-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d663a-129">OUTPUTS</span></span>

### <span data-ttu-id="d663a-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d663a-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="d663a-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="d663a-131">NOTES</span></span>

## <span data-ttu-id="d663a-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d663a-132">RELATED LINKS</span></span>
