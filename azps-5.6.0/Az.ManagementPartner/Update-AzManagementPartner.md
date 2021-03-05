---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 493f4b3e1cfaa3be59d0bd402e2c0d13dfdfad4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006686"
---
# <span data-ttu-id="37827-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="37827-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="37827-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37827-102">SYNOPSIS</span></span>
<span data-ttu-id="37827-103">Aggiorna l'ID Microsoft Partner Network (MPN) dell'utente autenticato corrente o dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="37827-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="37827-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37827-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37827-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="37827-105">DESCRIPTION</span></span>
<span data-ttu-id="37827-106">Aggiorna l'ID Microsoft Partner Network (MPN) dell'utente autenticato corrente o dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="37827-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="37827-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37827-107">EXAMPLES</span></span>

### <span data-ttu-id="37827-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="37827-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="37827-109">Aggiornare il partner di gestione a uno nuovo</span><span class="sxs-lookup"><span data-stu-id="37827-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="37827-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37827-110">PARAMETERS</span></span>

### <span data-ttu-id="37827-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37827-111">-DefaultProfile</span></span>
<span data-ttu-id="37827-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37827-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37827-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="37827-113">-PartnerId</span></span>
<span data-ttu-id="37827-114">ID del partner di gestione, è un numero di 6 cifre</span><span class="sxs-lookup"><span data-stu-id="37827-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="37827-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37827-115">-Confirm</span></span>
<span data-ttu-id="37827-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37827-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37827-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37827-117">-WhatIf</span></span>
<span data-ttu-id="37827-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37827-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37827-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37827-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37827-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37827-120">CommonParameters</span></span>
<span data-ttu-id="37827-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37827-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37827-122">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37827-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37827-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="37827-123">INPUTS</span></span>

### <span data-ttu-id="37827-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="37827-124">None</span></span>

## <span data-ttu-id="37827-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37827-125">OUTPUTS</span></span>

### <span data-ttu-id="37827-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="37827-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="37827-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="37827-127">NOTES</span></span>

## <span data-ttu-id="37827-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37827-128">RELATED LINKS</span></span>

[<span data-ttu-id="37827-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="37827-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="37827-130">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="37827-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="37827-131">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="37827-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)