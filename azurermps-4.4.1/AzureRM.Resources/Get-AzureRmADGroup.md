---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 1079486422da769863e86d3fc16d1c3ec65d6f5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513007"
---
# <span data-ttu-id="63f61-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="63f61-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="63f61-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="63f61-102">SYNOPSIS</span></span>
<span data-ttu-id="63f61-103">Filtra i gruppi di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="63f61-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63f61-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63f61-104">SYNTAX</span></span>

### <span data-ttu-id="63f61-105">EmptyParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="63f61-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63f61-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="63f61-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63f61-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63f61-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63f61-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63f61-108">DESCRIPTION</span></span>
<span data-ttu-id="63f61-109">Filtra i gruppi di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="63f61-109">Filters active directory groups.</span></span>

## <span data-ttu-id="63f61-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63f61-110">EXAMPLES</span></span>

### <span data-ttu-id="63f61-111">--------------------------Filtra i gruppi con l'ID oggetto--------------------------</span><span class="sxs-lookup"><span data-stu-id="63f61-111">--------------------------  Filters groups using object id  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="63f61-112">Ottiene il gruppo con ID 85F89C90-780E-4AA6-9F4F-6F268D322EEE</span><span class="sxs-lookup"><span data-stu-id="63f61-112">Gets group with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

### <span data-ttu-id="63f61-113">--------------------------Filtra i gruppi tramite la stringa di ricerca--------------------------</span><span class="sxs-lookup"><span data-stu-id="63f61-113">--------------------------  Filters groups using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="63f61-114">Filtra tutti i gruppi di annunci con Joe nel nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="63f61-114">Filters all ad groups that has Joe in the display name.</span></span>

### <span data-ttu-id="63f61-115">--------------------------Elenco gruppi di annunci--------------------------</span><span class="sxs-lookup"><span data-stu-id="63f61-115">--------------------------  List AD groups  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="63f61-116">Ottiene tutti i gruppi di annunci</span><span class="sxs-lookup"><span data-stu-id="63f61-116">Gets all AD groups</span></span>

## <span data-ttu-id="63f61-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="63f61-117">PARAMETERS</span></span>

### <span data-ttu-id="63f61-118">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="63f61-118">-ObjectId</span></span>
<span data-ttu-id="63f61-119">ID oggetto del gruppo.</span><span class="sxs-lookup"><span data-stu-id="63f61-119">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63f61-120">-SearchString</span><span class="sxs-lookup"><span data-stu-id="63f61-120">-SearchString</span></span>
<span data-ttu-id="63f61-121">Nome visualizzato del gruppo</span><span class="sxs-lookup"><span data-stu-id="63f61-121">The group display name</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63f61-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f61-122">-DefaultProfile</span></span>
<span data-ttu-id="63f61-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="63f61-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f61-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f61-124">CommonParameters</span></span>
<span data-ttu-id="63f61-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63f61-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f61-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63f61-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f61-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="63f61-127">INPUTS</span></span>

## <span data-ttu-id="63f61-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63f61-128">OUTPUTS</span></span>

### <span data-ttu-id="63f61-129">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup]</span><span class="sxs-lookup"><span data-stu-id="63f61-129">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup]</span></span>

## <span data-ttu-id="63f61-130">Note</span><span class="sxs-lookup"><span data-stu-id="63f61-130">NOTES</span></span>

## <span data-ttu-id="63f61-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63f61-131">RELATED LINKS</span></span>

[<span data-ttu-id="63f61-132">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="63f61-132">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="63f61-133">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="63f61-133">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="63f61-134">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="63f61-134">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

