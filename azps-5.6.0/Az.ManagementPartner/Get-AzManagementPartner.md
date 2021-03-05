---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: e09e63ed68ac87156fd03f73c992043b8a0271cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983085"
---
# <span data-ttu-id="0ed3c-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0ed3c-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="0ed3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ed3c-102">SYNOPSIS</span></span>
<span data-ttu-id="0ed3c-103">Ottiene l'ID Microsoft Partner Network (MPN) dell'utente autenticato corrente o dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="0ed3c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ed3c-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ed3c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0ed3c-105">DESCRIPTION</span></span>
<span data-ttu-id="0ed3c-106">Ottiene l'ID Microsoft Partner Network (MPN) dell'utente autenticato corrente o dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="0ed3c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ed3c-107">EXAMPLES</span></span>

### <span data-ttu-id="0ed3c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0ed3c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="0ed3c-109">Ottenere l'ID del partner di gestione corrente</span><span class="sxs-lookup"><span data-stu-id="0ed3c-109">Get the current management partner id</span></span>

### <span data-ttu-id="0ed3c-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0ed3c-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="0ed3c-111">Ottenere l'ID partner di gestione corrente usando un ID partner. Se non corrispondono, l'operazione non riesce</span><span class="sxs-lookup"><span data-stu-id="0ed3c-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="0ed3c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ed3c-112">PARAMETERS</span></span>

### <span data-ttu-id="0ed3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ed3c-113">-DefaultProfile</span></span>
<span data-ttu-id="0ed3c-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ed3c-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="0ed3c-115">-PartnerId</span></span>
<span data-ttu-id="0ed3c-116">ID del partner di gestione, è un numero di 6 cifre</span><span class="sxs-lookup"><span data-stu-id="0ed3c-116">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed3c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ed3c-117">CommonParameters</span></span>
<span data-ttu-id="0ed3c-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ed3c-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ed3c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ed3c-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="0ed3c-120">INPUTS</span></span>

### <span data-ttu-id="0ed3c-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0ed3c-121">None</span></span>

## <span data-ttu-id="0ed3c-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ed3c-122">OUTPUTS</span></span>

### <span data-ttu-id="0ed3c-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0ed3c-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="0ed3c-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="0ed3c-124">NOTES</span></span>

## <span data-ttu-id="0ed3c-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ed3c-125">RELATED LINKS</span></span>

[<span data-ttu-id="0ed3c-126">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0ed3c-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="0ed3c-127">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0ed3c-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="0ed3c-128">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0ed3c-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)