---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 6496f2c65c5cfecb01ed68d0e47281fba72b7b63
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022417"
---
# <span data-ttu-id="a945b-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="a945b-101">New-AzADGroup</span></span>

## <span data-ttu-id="a945b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a945b-102">SYNOPSIS</span></span>
<span data-ttu-id="a945b-103">Crea un nuovo gruppo di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a945b-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="a945b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a945b-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a945b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a945b-105">DESCRIPTION</span></span>
<span data-ttu-id="a945b-106">Crea un nuovo gruppo di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a945b-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="a945b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a945b-107">EXAMPLES</span></span>

### <span data-ttu-id="a945b-108">Esempio 1-creare un nuovo gruppo di annunci</span><span class="sxs-lookup"><span data-stu-id="a945b-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="a945b-109">Crea un nuovo gruppo di annunci con il nome "MyGroupDisplayName" e il Nickname di posta "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="a945b-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="a945b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a945b-110">PARAMETERS</span></span>

### <span data-ttu-id="a945b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a945b-111">-DefaultProfile</span></span>
<span data-ttu-id="a945b-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a945b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a945b-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="a945b-113">-Description</span></span>
<span data-ttu-id="a945b-114">Descrizione del gruppo.</span><span class="sxs-lookup"><span data-stu-id="a945b-114">The description for the group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a945b-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a945b-115">-DisplayName</span></span>
<span data-ttu-id="a945b-116">Nome visualizzato per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="a945b-116">The display name for the group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a945b-117">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="a945b-117">-MailNickname</span></span>
<span data-ttu-id="a945b-118">Nickname di posta per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="a945b-118">The mail nickname for the group.</span></span> <span data-ttu-id="a945b-119">Non può contenere il simbolo @.</span><span class="sxs-lookup"><span data-stu-id="a945b-119">Cannot contain the @ sign.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a945b-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a945b-120">-Confirm</span></span>
<span data-ttu-id="a945b-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a945b-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a945b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a945b-122">-WhatIf</span></span>
<span data-ttu-id="a945b-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a945b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a945b-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a945b-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a945b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a945b-125">CommonParameters</span></span>
<span data-ttu-id="a945b-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a945b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a945b-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a945b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a945b-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a945b-128">INPUTS</span></span>

### <span data-ttu-id="a945b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a945b-129">System.String</span></span>

## <span data-ttu-id="a945b-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a945b-130">OUTPUTS</span></span>

### <span data-ttu-id="a945b-131">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="a945b-131">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="a945b-132">Note</span><span class="sxs-lookup"><span data-stu-id="a945b-132">NOTES</span></span>

## <span data-ttu-id="a945b-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a945b-133">RELATED LINKS</span></span>
