---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
ms.openlocfilehash: c3a783178bf8342e891f8eab2996e77a2045721a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687016"
---
# <span data-ttu-id="33d29-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="33d29-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="33d29-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="33d29-102">SYNOPSIS</span></span>
<span data-ttu-id="33d29-103">Ottenere un membro del gruppo.</span><span class="sxs-lookup"><span data-stu-id="33d29-103">Get a group members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33d29-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33d29-104">SYNTAX</span></span>

```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33d29-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33d29-105">DESCRIPTION</span></span>
<span data-ttu-id="33d29-106">Ottenere un membro del gruppo.</span><span class="sxs-lookup"><span data-stu-id="33d29-106">Get a group members.</span></span>

## <span data-ttu-id="33d29-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33d29-107">EXAMPLES</span></span>

### <span data-ttu-id="33d29-108">Filtra i membri del gruppo usando l'ID oggetto gruppo</span><span class="sxs-lookup"><span data-stu-id="33d29-108">Filters group members using group object id</span></span>
```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="33d29-109">Ottiene i membri del gruppo con ID 85F89C90-780E-4AA6-9F4F-6F268D322EEE</span><span class="sxs-lookup"><span data-stu-id="33d29-109">Gets group members with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

## <span data-ttu-id="33d29-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="33d29-110">PARAMETERS</span></span>

### <span data-ttu-id="33d29-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d29-111">-DefaultProfile</span></span>
<span data-ttu-id="33d29-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="33d29-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33d29-113">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="33d29-113">-GroupObjectId</span></span>
<span data-ttu-id="33d29-114">ID oggetto del gruppo.</span><span class="sxs-lookup"><span data-stu-id="33d29-114">Object id of the group.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33d29-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d29-115">CommonParameters</span></span>
<span data-ttu-id="33d29-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33d29-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d29-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33d29-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d29-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="33d29-118">INPUTS</span></span>

### <span data-ttu-id="33d29-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="33d29-119">None</span></span>
<span data-ttu-id="33d29-120">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="33d29-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33d29-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33d29-121">OUTPUTS</span></span>

### <span data-ttu-id="33d29-122">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADObject]</span><span class="sxs-lookup"><span data-stu-id="33d29-122">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject]</span></span>

## <span data-ttu-id="33d29-123">Note</span><span class="sxs-lookup"><span data-stu-id="33d29-123">NOTES</span></span>

## <span data-ttu-id="33d29-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33d29-124">RELATED LINKS</span></span>

[<span data-ttu-id="33d29-125">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="33d29-125">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="33d29-126">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="33d29-126">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

