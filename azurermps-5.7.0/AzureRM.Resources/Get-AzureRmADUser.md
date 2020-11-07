---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: e111da68e00e0edad54823c763c06f84ea5100e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686698"
---
# <span data-ttu-id="d8ced-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="d8ced-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="d8ced-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d8ced-102">SYNOPSIS</span></span>
<span data-ttu-id="d8ced-103">Filtra gli utenti di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d8ced-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8ced-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8ced-104">SYNTAX</span></span>

### <span data-ttu-id="d8ced-105">EmptyParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d8ced-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8ced-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8ced-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8ced-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8ced-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8ced-108">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8ced-108">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8ced-109">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8ced-109">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8ced-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8ced-110">DESCRIPTION</span></span>
<span data-ttu-id="d8ced-111">Filtra gli utenti di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d8ced-111">Filters active directory users.</span></span>

## <span data-ttu-id="d8ced-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8ced-112">EXAMPLES</span></span>

### <span data-ttu-id="d8ced-113">Filtra gli utenti con UPN</span><span class="sxs-lookup"><span data-stu-id="d8ced-113">Filters users using UPN</span></span>
```
PS C:\> Get-AzureRmADUser -UPN foo@domain.com
```

<span data-ttu-id="d8ced-114">Ottiene l'utente con foo@domain.com</span><span class="sxs-lookup"><span data-stu-id="d8ced-114">Gets user with foo@domain.com</span></span>

### <span data-ttu-id="d8ced-115">Filtra gli utenti con la stringa di ricerca</span><span class="sxs-lookup"><span data-stu-id="d8ced-115">Filters users using Search String</span></span>
```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="d8ced-116">Filtra tutti gli utenti di Active Directory con Joe nel nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="d8ced-116">Filters all ad users that has Joe in the display name.</span></span>

### <span data-ttu-id="d8ced-117">Elencare gli utenti degli annunci</span><span class="sxs-lookup"><span data-stu-id="d8ced-117">List AD users</span></span>
```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="d8ced-118">Ottiene tutti gli utenti di Active Directory</span><span class="sxs-lookup"><span data-stu-id="d8ced-118">Gets all AD users</span></span>

## <span data-ttu-id="d8ced-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8ced-119">PARAMETERS</span></span>

### <span data-ttu-id="d8ced-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8ced-120">-DefaultProfile</span></span>
<span data-ttu-id="d8ced-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d8ced-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8ced-122">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="d8ced-122">-Mail</span></span>
```yaml
Type: String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8ced-123">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d8ced-123">-ObjectId</span></span>
<span data-ttu-id="d8ced-124">ID oggetto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d8ced-124">Object id of the user.</span></span>

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

### <span data-ttu-id="d8ced-125">-SearchString</span><span class="sxs-lookup"><span data-stu-id="d8ced-125">-SearchString</span></span>
<span data-ttu-id="d8ced-126">Nome visualizzato dell'utente</span><span class="sxs-lookup"><span data-stu-id="d8ced-126">The user display name</span></span>

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

### <span data-ttu-id="d8ced-127">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d8ced-127">-UserPrincipalName</span></span>
<span data-ttu-id="d8ced-128">UPN dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d8ced-128">UPN of the user.</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8ced-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8ced-129">CommonParameters</span></span>
<span data-ttu-id="d8ced-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8ced-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8ced-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8ced-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8ced-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d8ced-132">INPUTS</span></span>

### <span data-ttu-id="d8ced-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d8ced-133">None</span></span>
<span data-ttu-id="d8ced-134">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d8ced-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d8ced-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8ced-135">OUTPUTS</span></span>

### <span data-ttu-id="d8ced-136">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser]</span><span class="sxs-lookup"><span data-stu-id="d8ced-136">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser]</span></span>

## <span data-ttu-id="d8ced-137">Note</span><span class="sxs-lookup"><span data-stu-id="d8ced-137">NOTES</span></span>

## <span data-ttu-id="d8ced-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8ced-138">RELATED LINKS</span></span>

[<span data-ttu-id="d8ced-139">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="d8ced-139">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="d8ced-140">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="d8ced-140">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="d8ced-141">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="d8ced-141">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

