---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 98d87c060c51d19db45e907f88d39f27350248c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032810"
---
# <span data-ttu-id="5529c-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="5529c-101">New-AzADGroup</span></span>

## <span data-ttu-id="5529c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5529c-102">SYNOPSIS</span></span>
<span data-ttu-id="5529c-103">Crea un nuovo gruppo di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5529c-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="5529c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5529c-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5529c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5529c-105">DESCRIPTION</span></span>
<span data-ttu-id="5529c-106">Crea un nuovo gruppo di Active Directory. Di seguito sono elencate le autorizzazioni necessarie:</span><span class="sxs-lookup"><span data-stu-id="5529c-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="5529c-107">Grafico di Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="5529c-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="5529c-108">Directory. ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="5529c-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="5529c-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="5529c-109">Microsoft Graph</span></span>
  - <span data-ttu-id="5529c-110">Directory. ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="5529c-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="5529c-111">PrivilegedAccess. ReadWrite. AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="5529c-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="5529c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5529c-112">EXAMPLES</span></span>

### <span data-ttu-id="5529c-113">Esempio 1: creare un nuovo gruppo di annunci</span><span class="sxs-lookup"><span data-stu-id="5529c-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="5529c-114">Crea un nuovo gruppo di annunci con il nome "MyGroupDisplayName" e il Nickname di posta "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="5529c-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="5529c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5529c-115">PARAMETERS</span></span>

### <span data-ttu-id="5529c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5529c-116">-DefaultProfile</span></span>
<span data-ttu-id="5529c-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5529c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5529c-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="5529c-118">-Description</span></span>
<span data-ttu-id="5529c-119">Descrizione del gruppo.</span><span class="sxs-lookup"><span data-stu-id="5529c-119">The description for the group.</span></span>

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

### <span data-ttu-id="5529c-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5529c-120">-DisplayName</span></span>
<span data-ttu-id="5529c-121">Nome visualizzato per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="5529c-121">The display name for the group.</span></span>

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

### <span data-ttu-id="5529c-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="5529c-122">-MailNickname</span></span>
<span data-ttu-id="5529c-123">Nickname di posta per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="5529c-123">The mail nickname for the group.</span></span> <span data-ttu-id="5529c-124">Non può contenere il simbolo @.</span><span class="sxs-lookup"><span data-stu-id="5529c-124">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="5529c-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5529c-125">-Confirm</span></span>
<span data-ttu-id="5529c-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5529c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5529c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5529c-127">-WhatIf</span></span>
<span data-ttu-id="5529c-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5529c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5529c-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5529c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5529c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5529c-130">CommonParameters</span></span>
<span data-ttu-id="5529c-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5529c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5529c-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5529c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5529c-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5529c-133">INPUTS</span></span>

### <span data-ttu-id="5529c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5529c-134">System.String</span></span>

## <span data-ttu-id="5529c-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5529c-135">OUTPUTS</span></span>

### <span data-ttu-id="5529c-136">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="5529c-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="5529c-137">Note</span><span class="sxs-lookup"><span data-stu-id="5529c-137">NOTES</span></span>

## <span data-ttu-id="5529c-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5529c-138">RELATED LINKS</span></span>
