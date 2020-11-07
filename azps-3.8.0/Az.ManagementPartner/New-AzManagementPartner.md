---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/new-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
ms.openlocfilehash: 9e6c56fa48b71e2571b7702e170bdc3e9e41f3aa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864418"
---
# <span data-ttu-id="d15c3-101">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="d15c3-101">New-AzManagementPartner</span></span>

## <span data-ttu-id="d15c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d15c3-102">SYNOPSIS</span></span>
<span data-ttu-id="d15c3-103">Associa un ID Microsoft Partner Network (MPN) all'utente autenticato o all'entità di servizio corrente.</span><span class="sxs-lookup"><span data-stu-id="d15c3-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="d15c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d15c3-104">SYNTAX</span></span>

```
New-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d15c3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d15c3-105">DESCRIPTION</span></span>
<span data-ttu-id="d15c3-106">Associa un ID Microsoft Partner Network (MPN) all'utente autenticato o all'entità di servizio corrente.</span><span class="sxs-lookup"><span data-stu-id="d15c3-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="d15c3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d15c3-107">EXAMPLES</span></span>

### <span data-ttu-id="d15c3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d15c3-108">Example 1</span></span>
```powershell
PS C:\> New-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="d15c3-109">Aggiungere un partner di gestione</span><span class="sxs-lookup"><span data-stu-id="d15c3-109">Add a management partner</span></span>

## <span data-ttu-id="d15c3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d15c3-110">PARAMETERS</span></span>

### <span data-ttu-id="d15c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d15c3-111">-DefaultProfile</span></span>
<span data-ttu-id="d15c3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d15c3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d15c3-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="d15c3-113">-PartnerId</span></span>
<span data-ttu-id="d15c3-114">L'ID del partner di gestione è un numero a 6 cifre</span><span class="sxs-lookup"><span data-stu-id="d15c3-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="d15c3-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d15c3-115">-Confirm</span></span>
<span data-ttu-id="d15c3-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d15c3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d15c3-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d15c3-117">-WhatIf</span></span>
<span data-ttu-id="d15c3-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d15c3-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d15c3-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d15c3-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d15c3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d15c3-120">CommonParameters</span></span>
<span data-ttu-id="d15c3-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d15c3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d15c3-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d15c3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d15c3-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d15c3-123">INPUTS</span></span>

### <span data-ttu-id="d15c3-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d15c3-124">None</span></span>

## <span data-ttu-id="d15c3-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d15c3-125">OUTPUTS</span></span>

### <span data-ttu-id="d15c3-126">Microsoft. Azure. Commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="d15c3-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="d15c3-127">Note</span><span class="sxs-lookup"><span data-stu-id="d15c3-127">NOTES</span></span>

## <span data-ttu-id="d15c3-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d15c3-128">RELATED LINKS</span></span>

[<span data-ttu-id="d15c3-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="d15c3-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="d15c3-130">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="d15c3-130">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="d15c3-131">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="d15c3-131">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)