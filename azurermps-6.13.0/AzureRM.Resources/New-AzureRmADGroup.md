---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADGroup.md
ms.openlocfilehash: 751b1b7daff59861b3f8e480b27dc4c88d35709d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514835"
---
# <span data-ttu-id="96555-101">New-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="96555-101">New-AzureRmADGroup</span></span>

## <span data-ttu-id="96555-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96555-102">SYNOPSIS</span></span>
<span data-ttu-id="96555-103">Crea un nuovo gruppo di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="96555-103">Creates a new active directory group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96555-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96555-104">SYNTAX</span></span>

```
New-AzureRmADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96555-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96555-105">DESCRIPTION</span></span>
<span data-ttu-id="96555-106">Crea un nuovo gruppo di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="96555-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="96555-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96555-107">EXAMPLES</span></span>

### <span data-ttu-id="96555-108">Esempio 1-creare un nuovo gruppo di annunci</span><span class="sxs-lookup"><span data-stu-id="96555-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzureRmADGroup -DisplayName "MyGroupDisplayName" -MailNickname "myemail@domain.com"
```

<span data-ttu-id="96555-109">Crea un nuovo gruppo di annunci con il nome "MyGroupDisplayName" e il Nickname di posta " myemail@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="96555-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "myemail@domain.com".</span></span>

## <span data-ttu-id="96555-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96555-110">PARAMETERS</span></span>

### <span data-ttu-id="96555-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96555-111">-DefaultProfile</span></span>
<span data-ttu-id="96555-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96555-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96555-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="96555-113">-DisplayName</span></span>
<span data-ttu-id="96555-114">Nome visualizzato per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="96555-114">The display name for the group.</span></span>

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

### <span data-ttu-id="96555-115">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="96555-115">-MailNickname</span></span>
<span data-ttu-id="96555-116">Nickname di posta per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="96555-116">The mail nickname for the group.</span></span>

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

### <span data-ttu-id="96555-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="96555-117">-Confirm</span></span>
<span data-ttu-id="96555-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96555-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96555-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96555-119">-WhatIf</span></span>
<span data-ttu-id="96555-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96555-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96555-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96555-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96555-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96555-122">CommonParameters</span></span>
<span data-ttu-id="96555-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96555-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96555-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96555-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96555-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96555-125">INPUTS</span></span>

### <span data-ttu-id="96555-126">System. String</span><span class="sxs-lookup"><span data-stu-id="96555-126">System.String</span></span>

## <span data-ttu-id="96555-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96555-127">OUTPUTS</span></span>

### <span data-ttu-id="96555-128">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="96555-128">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="96555-129">Note</span><span class="sxs-lookup"><span data-stu-id="96555-129">NOTES</span></span>

## <span data-ttu-id="96555-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96555-130">RELATED LINKS</span></span>