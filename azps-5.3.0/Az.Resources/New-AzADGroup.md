---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 98d87c060c51d19db45e907f88d39f27350248c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474226"
---
# <span data-ttu-id="9c81f-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="9c81f-101">New-AzADGroup</span></span>

## <span data-ttu-id="9c81f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9c81f-102">SYNOPSIS</span></span>
<span data-ttu-id="9c81f-103">Crea un nuovo gruppo di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9c81f-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="9c81f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c81f-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c81f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c81f-105">DESCRIPTION</span></span>
<span data-ttu-id="9c81f-106">Crea un nuovo gruppo di Active Directory. Di seguito sono elencate le autorizzazioni necessarie:</span><span class="sxs-lookup"><span data-stu-id="9c81f-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="9c81f-107">Grafico di Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="9c81f-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="9c81f-108">Directory. ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="9c81f-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="9c81f-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="9c81f-109">Microsoft Graph</span></span>
  - <span data-ttu-id="9c81f-110">Directory. ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="9c81f-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="9c81f-111">PrivilegedAccess. ReadWrite. AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="9c81f-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="9c81f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c81f-112">EXAMPLES</span></span>

### <span data-ttu-id="9c81f-113">Esempio 1: creare un nuovo gruppo di annunci</span><span class="sxs-lookup"><span data-stu-id="9c81f-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="9c81f-114">Crea un nuovo gruppo di annunci con il nome "MyGroupDisplayName" e il Nickname di posta "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="9c81f-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="9c81f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9c81f-115">PARAMETERS</span></span>

### <span data-ttu-id="9c81f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c81f-116">-DefaultProfile</span></span>
<span data-ttu-id="9c81f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c81f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c81f-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c81f-118">-Description</span></span>
<span data-ttu-id="9c81f-119">Descrizione del gruppo.</span><span class="sxs-lookup"><span data-stu-id="9c81f-119">The description for the group.</span></span>

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

### <span data-ttu-id="9c81f-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9c81f-120">-DisplayName</span></span>
<span data-ttu-id="9c81f-121">Nome visualizzato per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="9c81f-121">The display name for the group.</span></span>

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

### <span data-ttu-id="9c81f-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="9c81f-122">-MailNickname</span></span>
<span data-ttu-id="9c81f-123">Nickname di posta per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="9c81f-123">The mail nickname for the group.</span></span> <span data-ttu-id="9c81f-124">Non può contenere il simbolo @.</span><span class="sxs-lookup"><span data-stu-id="9c81f-124">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="9c81f-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9c81f-125">-Confirm</span></span>
<span data-ttu-id="9c81f-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c81f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c81f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c81f-127">-WhatIf</span></span>
<span data-ttu-id="9c81f-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c81f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c81f-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c81f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c81f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c81f-130">CommonParameters</span></span>
<span data-ttu-id="9c81f-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c81f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c81f-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c81f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c81f-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9c81f-133">INPUTS</span></span>

### <span data-ttu-id="9c81f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9c81f-134">System.String</span></span>

## <span data-ttu-id="9c81f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c81f-135">OUTPUTS</span></span>

### <span data-ttu-id="9c81f-136">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="9c81f-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="9c81f-137">Note</span><span class="sxs-lookup"><span data-stu-id="9c81f-137">NOTES</span></span>

## <span data-ttu-id="9c81f-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c81f-138">RELATED LINKS</span></span>
