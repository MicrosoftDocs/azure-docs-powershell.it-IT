---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 98d87c060c51d19db45e907f88d39f27350248c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186454"
---
# <span data-ttu-id="36e95-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="36e95-101">New-AzADGroup</span></span>

## <span data-ttu-id="36e95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36e95-102">SYNOPSIS</span></span>
<span data-ttu-id="36e95-103">Crea un nuovo gruppo active directory.</span><span class="sxs-lookup"><span data-stu-id="36e95-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="36e95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36e95-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36e95-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="36e95-105">DESCRIPTION</span></span>
<span data-ttu-id="36e95-106">Crea un nuovo gruppo active directory. Di seguito sono elencate le autorizzazioni necessarie:</span><span class="sxs-lookup"><span data-stu-id="36e95-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="36e95-107">Azure Active Directory Graph</span><span class="sxs-lookup"><span data-stu-id="36e95-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="36e95-108">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="36e95-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="36e95-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="36e95-109">Microsoft Graph</span></span>
  - <span data-ttu-id="36e95-110">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="36e95-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="36e95-111">PrivilegedAccess.ReadWrite.AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="36e95-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="36e95-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36e95-112">EXAMPLES</span></span>

### <span data-ttu-id="36e95-113">Esempio 1: Creare un nuovo gruppo di Active Directory</span><span class="sxs-lookup"><span data-stu-id="36e95-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="36e95-114">Crea un nuovo gruppo Active Directory con il nome "MyGroupDisplayName" e il nome alternativo per la posta "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="36e95-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="36e95-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36e95-115">PARAMETERS</span></span>

### <span data-ttu-id="36e95-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e95-116">-DefaultProfile</span></span>
<span data-ttu-id="36e95-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36e95-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36e95-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="36e95-118">-Description</span></span>
<span data-ttu-id="36e95-119">Descrizione del gruppo.</span><span class="sxs-lookup"><span data-stu-id="36e95-119">The description for the group.</span></span>

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

### <span data-ttu-id="36e95-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="36e95-120">-DisplayName</span></span>
<span data-ttu-id="36e95-121">Nome visualizzato per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="36e95-121">The display name for the group.</span></span>

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

### <span data-ttu-id="36e95-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="36e95-122">-MailNickname</span></span>
<span data-ttu-id="36e95-123">Il soprannome di posta elettronica per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="36e95-123">The mail nickname for the group.</span></span> <span data-ttu-id="36e95-124">Non può contenere il simbolo @.</span><span class="sxs-lookup"><span data-stu-id="36e95-124">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="36e95-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36e95-125">-Confirm</span></span>
<span data-ttu-id="36e95-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36e95-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36e95-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36e95-127">-WhatIf</span></span>
<span data-ttu-id="36e95-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36e95-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36e95-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36e95-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36e95-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e95-130">CommonParameters</span></span>
<span data-ttu-id="36e95-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36e95-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e95-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="36e95-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e95-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="36e95-133">INPUTS</span></span>

### <span data-ttu-id="36e95-134">System.String</span><span class="sxs-lookup"><span data-stu-id="36e95-134">System.String</span></span>

## <span data-ttu-id="36e95-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36e95-135">OUTPUTS</span></span>

### <span data-ttu-id="36e95-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="36e95-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="36e95-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="36e95-137">NOTES</span></span>

## <span data-ttu-id="36e95-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36e95-138">RELATED LINKS</span></span>
