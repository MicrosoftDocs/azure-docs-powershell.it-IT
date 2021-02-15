---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/new-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
ms.openlocfilehash: 9e6c56fa48b71e2571b7702e170bdc3e9e41f3aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203689"
---
# <span data-ttu-id="cd7c7-101">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="cd7c7-101">New-AzManagementPartner</span></span>

## <span data-ttu-id="cd7c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd7c7-102">SYNOPSIS</span></span>
<span data-ttu-id="cd7c7-103">Associa un ID Microsoft Partner Network (MPN) all'utente autenticato corrente o all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="cd7c7-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="cd7c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd7c7-104">SYNTAX</span></span>

```
New-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd7c7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cd7c7-105">DESCRIPTION</span></span>
<span data-ttu-id="cd7c7-106">Associa un ID Microsoft Partner Network (MPN) all'utente autenticato corrente o all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="cd7c7-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="cd7c7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd7c7-107">EXAMPLES</span></span>

### <span data-ttu-id="cd7c7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cd7c7-108">Example 1</span></span>
```powershell
PS C:\> New-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="cd7c7-109">Aggiungere un partner di gestione</span><span class="sxs-lookup"><span data-stu-id="cd7c7-109">Add a management partner</span></span>

## <span data-ttu-id="cd7c7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd7c7-110">PARAMETERS</span></span>

### <span data-ttu-id="cd7c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd7c7-111">-DefaultProfile</span></span>
<span data-ttu-id="cd7c7-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd7c7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd7c7-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="cd7c7-113">-PartnerId</span></span>
<span data-ttu-id="cd7c7-114">ID del partner di gestione, è un numero di 6 cifre</span><span class="sxs-lookup"><span data-stu-id="cd7c7-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd7c7-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd7c7-115">-Confirm</span></span>
<span data-ttu-id="cd7c7-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd7c7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd7c7-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd7c7-117">-WhatIf</span></span>
<span data-ttu-id="cd7c7-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd7c7-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd7c7-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd7c7-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd7c7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd7c7-120">CommonParameters</span></span>
<span data-ttu-id="cd7c7-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd7c7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd7c7-122">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd7c7-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd7c7-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="cd7c7-123">INPUTS</span></span>

### <span data-ttu-id="cd7c7-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cd7c7-124">None</span></span>

## <span data-ttu-id="cd7c7-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd7c7-125">OUTPUTS</span></span>

### <span data-ttu-id="cd7c7-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="cd7c7-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="cd7c7-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="cd7c7-127">NOTES</span></span>

## <span data-ttu-id="cd7c7-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd7c7-128">RELATED LINKS</span></span>

[<span data-ttu-id="cd7c7-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="cd7c7-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="cd7c7-130">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="cd7c7-130">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="cd7c7-131">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="cd7c7-131">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)