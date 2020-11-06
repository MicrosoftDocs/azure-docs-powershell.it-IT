---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 29c3a76817bd50a5f86ea051b6de1139980a0dba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519875"
---
# <span data-ttu-id="f3170-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="f3170-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="f3170-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3170-102">SYNOPSIS</span></span>
<span data-ttu-id="f3170-103">Filtra i gruppi di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f3170-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3170-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3170-104">SYNTAX</span></span>

### <span data-ttu-id="f3170-105">EmptyParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f3170-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3170-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3170-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3170-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3170-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3170-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3170-108">DESCRIPTION</span></span>
<span data-ttu-id="f3170-109">Filtra i gruppi di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f3170-109">Filters active directory groups.</span></span>

## <span data-ttu-id="f3170-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3170-110">EXAMPLES</span></span>

### <span data-ttu-id="f3170-111">Filtra i gruppi con l'ID oggetto</span><span class="sxs-lookup"><span data-stu-id="f3170-111">Filters groups using object id</span></span>
```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="f3170-112">Ottiene il gruppo con ID 85F89C90-780E-4AA6-9F4F-6F268D322EEE</span><span class="sxs-lookup"><span data-stu-id="f3170-112">Gets group with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

### <span data-ttu-id="f3170-113">Filtra i gruppi usando la stringa di ricerca</span><span class="sxs-lookup"><span data-stu-id="f3170-113">Filters groups using Search String</span></span>
```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="f3170-114">Filtra tutti i gruppi di annunci con Joe nel nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="f3170-114">Filters all ad groups that has Joe in the display name.</span></span>

### <span data-ttu-id="f3170-115">Gruppi di annunci elenco</span><span class="sxs-lookup"><span data-stu-id="f3170-115">List AD groups</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="f3170-116">Ottiene tutti i gruppi di annunci</span><span class="sxs-lookup"><span data-stu-id="f3170-116">Gets all AD groups</span></span>

## <span data-ttu-id="f3170-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3170-117">PARAMETERS</span></span>

### <span data-ttu-id="f3170-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3170-118">-DefaultProfile</span></span>
<span data-ttu-id="f3170-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f3170-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3170-120">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f3170-120">-ObjectId</span></span>
<span data-ttu-id="f3170-121">ID oggetto del gruppo.</span><span class="sxs-lookup"><span data-stu-id="f3170-121">Object id of the group.</span></span>

```yaml
Type: Guid
Parameter Sets: EmptyParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3170-122">-SearchString</span><span class="sxs-lookup"><span data-stu-id="f3170-122">-SearchString</span></span>
<span data-ttu-id="f3170-123">Nome visualizzato del gruppo</span><span class="sxs-lookup"><span data-stu-id="f3170-123">The group display name</span></span>

```yaml
Type: String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3170-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3170-124">CommonParameters</span></span>
<span data-ttu-id="f3170-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3170-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3170-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3170-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3170-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3170-127">INPUTS</span></span>

### <span data-ttu-id="f3170-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f3170-128">None</span></span>
<span data-ttu-id="f3170-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f3170-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f3170-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3170-130">OUTPUTS</span></span>

### <span data-ttu-id="f3170-131">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup]</span><span class="sxs-lookup"><span data-stu-id="f3170-131">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup]</span></span>

## <span data-ttu-id="f3170-132">Note</span><span class="sxs-lookup"><span data-stu-id="f3170-132">NOTES</span></span>

## <span data-ttu-id="f3170-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3170-133">RELATED LINKS</span></span>

[<span data-ttu-id="f3170-134">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="f3170-134">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="f3170-135">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f3170-135">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="f3170-136">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="f3170-136">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

