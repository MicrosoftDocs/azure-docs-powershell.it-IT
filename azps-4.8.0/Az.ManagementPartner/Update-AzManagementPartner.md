---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 326e16ff2f5bca8ca5ae987ebedf12cace87e11d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192418"
---
# <span data-ttu-id="9801c-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="9801c-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="9801c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9801c-102">SYNOPSIS</span></span>
<span data-ttu-id="9801c-103">Aggiorna l'ID Microsoft Partner Network (MPN) dell'utente o dell'entità di servizio corrente autenticato.</span><span class="sxs-lookup"><span data-stu-id="9801c-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="9801c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9801c-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9801c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9801c-105">DESCRIPTION</span></span>
<span data-ttu-id="9801c-106">Aggiorna l'ID Microsoft Partner Network (MPN) dell'utente o dell'entità di servizio corrente autenticato.</span><span class="sxs-lookup"><span data-stu-id="9801c-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="9801c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9801c-107">EXAMPLES</span></span>

### <span data-ttu-id="9801c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9801c-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="9801c-109">Aggiornare il partner di gestione in uno nuovo</span><span class="sxs-lookup"><span data-stu-id="9801c-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="9801c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9801c-110">PARAMETERS</span></span>

### <span data-ttu-id="9801c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9801c-111">-DefaultProfile</span></span>
<span data-ttu-id="9801c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9801c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9801c-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="9801c-113">-PartnerId</span></span>
<span data-ttu-id="9801c-114">L'ID del partner di gestione è un numero a 6 cifre</span><span class="sxs-lookup"><span data-stu-id="9801c-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="9801c-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9801c-115">-Confirm</span></span>
<span data-ttu-id="9801c-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9801c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9801c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9801c-117">-WhatIf</span></span>
<span data-ttu-id="9801c-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9801c-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9801c-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9801c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9801c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9801c-120">CommonParameters</span></span>
<span data-ttu-id="9801c-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9801c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9801c-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9801c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9801c-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9801c-123">INPUTS</span></span>

### <span data-ttu-id="9801c-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9801c-124">None</span></span>

## <span data-ttu-id="9801c-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9801c-125">OUTPUTS</span></span>

### <span data-ttu-id="9801c-126">Microsoft. Azure. Commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="9801c-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="9801c-127">Note</span><span class="sxs-lookup"><span data-stu-id="9801c-127">NOTES</span></span>

## <span data-ttu-id="9801c-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9801c-128">RELATED LINKS</span></span>

[<span data-ttu-id="9801c-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="9801c-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="9801c-130">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="9801c-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="9801c-131">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="9801c-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)