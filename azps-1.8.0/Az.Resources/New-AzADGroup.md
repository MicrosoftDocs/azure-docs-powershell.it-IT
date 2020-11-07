---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 50cb6a806522e8e8b0f3a792ad74e2543633f668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677364"
---
# <span data-ttu-id="a2418-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="a2418-101">New-AzADGroup</span></span>

## <span data-ttu-id="a2418-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a2418-102">SYNOPSIS</span></span>
<span data-ttu-id="a2418-103">Crea un nuovo gruppo di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a2418-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="a2418-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2418-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2418-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2418-105">DESCRIPTION</span></span>
<span data-ttu-id="a2418-106">Crea un nuovo gruppo di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a2418-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="a2418-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2418-107">EXAMPLES</span></span>

### <span data-ttu-id="a2418-108">Esempio 1-creare un nuovo gruppo di annunci</span><span class="sxs-lookup"><span data-stu-id="a2418-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="a2418-109">Crea un nuovo gruppo di annunci con il nome "MyGroupDisplayName" e il Nickname di posta "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="a2418-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="a2418-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a2418-110">PARAMETERS</span></span>

### <span data-ttu-id="a2418-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2418-111">-DefaultProfile</span></span>
<span data-ttu-id="a2418-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a2418-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2418-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a2418-113">-DisplayName</span></span>
<span data-ttu-id="a2418-114">Nome visualizzato per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="a2418-114">The display name for the group.</span></span>

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

### <span data-ttu-id="a2418-115">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="a2418-115">-MailNickname</span></span>
<span data-ttu-id="a2418-116">Nickname di posta per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="a2418-116">The mail nickname for the group.</span></span> <span data-ttu-id="a2418-117">Non può contenere il simbolo @.</span><span class="sxs-lookup"><span data-stu-id="a2418-117">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="a2418-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a2418-118">-Confirm</span></span>
<span data-ttu-id="a2418-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2418-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2418-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2418-120">-WhatIf</span></span>
<span data-ttu-id="a2418-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2418-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2418-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2418-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2418-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2418-123">CommonParameters</span></span>
<span data-ttu-id="a2418-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2418-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2418-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2418-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2418-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a2418-126">INPUTS</span></span>

### <span data-ttu-id="a2418-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a2418-127">System.String</span></span>

## <span data-ttu-id="a2418-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2418-128">OUTPUTS</span></span>

### <span data-ttu-id="a2418-129">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="a2418-129">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="a2418-130">Note</span><span class="sxs-lookup"><span data-stu-id="a2418-130">NOTES</span></span>

## <span data-ttu-id="a2418-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2418-131">RELATED LINKS</span></span>
