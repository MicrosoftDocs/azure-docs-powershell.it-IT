---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: 1031c9c8828969d16097953aa7440e2c8c0a8c1b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368199"
---
# <span data-ttu-id="f99f7-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="f99f7-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="f99f7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f99f7-102">SYNOPSIS</span></span>
<span data-ttu-id="f99f7-103">Ottiene l'ID Microsoft Partner Network (MPN) dell'utente autenticato o dell'entità di servizio corrente.</span><span class="sxs-lookup"><span data-stu-id="f99f7-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="f99f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f99f7-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f99f7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f99f7-105">DESCRIPTION</span></span>
<span data-ttu-id="f99f7-106">Ottiene l'ID Microsoft Partner Network (MPN) dell'utente autenticato o dell'entità di servizio corrente.</span><span class="sxs-lookup"><span data-stu-id="f99f7-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="f99f7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f99f7-107">EXAMPLES</span></span>

### <span data-ttu-id="f99f7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f99f7-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="f99f7-109">Ottenere l'ID del partner di gestione corrente</span><span class="sxs-lookup"><span data-stu-id="f99f7-109">Get the current management partner id</span></span>

### <span data-ttu-id="f99f7-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f99f7-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="f99f7-111">Ottenere l'ID del partner di gestione corrente con un ID partner, se non corrispondono, non riesce</span><span class="sxs-lookup"><span data-stu-id="f99f7-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="f99f7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f99f7-112">PARAMETERS</span></span>

### <span data-ttu-id="f99f7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f99f7-113">-DefaultProfile</span></span>
<span data-ttu-id="f99f7-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f99f7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f99f7-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="f99f7-115">-PartnerId</span></span>
<span data-ttu-id="f99f7-116">L'ID del partner di gestione è un numero a 6 cifre</span><span class="sxs-lookup"><span data-stu-id="f99f7-116">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="f99f7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f99f7-117">CommonParameters</span></span>
<span data-ttu-id="f99f7-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f99f7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f99f7-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f99f7-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f99f7-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f99f7-120">INPUTS</span></span>

### <span data-ttu-id="f99f7-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f99f7-121">None</span></span>

## <span data-ttu-id="f99f7-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f99f7-122">OUTPUTS</span></span>

### <span data-ttu-id="f99f7-123">Microsoft. Azure. Commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="f99f7-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="f99f7-124">Note</span><span class="sxs-lookup"><span data-stu-id="f99f7-124">NOTES</span></span>

## <span data-ttu-id="f99f7-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f99f7-125">RELATED LINKS</span></span>

[<span data-ttu-id="f99f7-126">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="f99f7-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="f99f7-127">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="f99f7-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="f99f7-128">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="f99f7-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)