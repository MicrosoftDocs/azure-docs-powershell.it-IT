---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/get-azurermmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Get-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Get-AzureRmManagementPartner.md
ms.openlocfilehash: b1fe94533074860a3c95c05d6609bb8ebb446a9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516744"
---
# <span data-ttu-id="2cfe0-101">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="2cfe0-101">Get-AzureRmManagementPartner</span></span>

## <span data-ttu-id="2cfe0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2cfe0-102">SYNOPSIS</span></span>
<span data-ttu-id="2cfe0-103">Ottiene l'ID Microsoft Partner Network (MPN) dell'utente autenticato o dell'entità di servizio corrente.</span><span class="sxs-lookup"><span data-stu-id="2cfe0-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cfe0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2cfe0-104">SYNTAX</span></span>

```
Get-AzureRmManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2cfe0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2cfe0-105">DESCRIPTION</span></span>
<span data-ttu-id="2cfe0-106">Ottiene l'ID Microsoft Partner Network (MPN) dell'utente autenticato o dell'entità di servizio corrente.</span><span class="sxs-lookup"><span data-stu-id="2cfe0-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span> 

## <span data-ttu-id="2cfe0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2cfe0-107">EXAMPLES</span></span>

### <span data-ttu-id="2cfe0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2cfe0-108">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="2cfe0-109">Ottenere l'ID del partner di gestione corrente</span><span class="sxs-lookup"><span data-stu-id="2cfe0-109">Get the current management partner id</span></span>

### <span data-ttu-id="2cfe0-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2cfe0-110">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="2cfe0-111">Ottenere l'ID del partner di gestione corrente con un ID partner, se non corrispondono, non riesce</span><span class="sxs-lookup"><span data-stu-id="2cfe0-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="2cfe0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2cfe0-112">PARAMETERS</span></span>

### <span data-ttu-id="2cfe0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cfe0-113">-DefaultProfile</span></span>
<span data-ttu-id="2cfe0-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2cfe0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfe0-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="2cfe0-115">-PartnerId</span></span>
<span data-ttu-id="2cfe0-116">L'ID del partner di gestione è un numero a 6 cifre</span><span class="sxs-lookup"><span data-stu-id="2cfe0-116">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfe0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cfe0-117">CommonParameters</span></span>
<span data-ttu-id="2cfe0-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cfe0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cfe0-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cfe0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cfe0-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2cfe0-120">INPUTS</span></span>

### <span data-ttu-id="2cfe0-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2cfe0-121">None</span></span>

## <span data-ttu-id="2cfe0-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2cfe0-122">OUTPUTS</span></span>

### <span data-ttu-id="2cfe0-123">Microsoft. Azure. Commands. resources. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="2cfe0-123">Microsoft.Azure.Commands.Resources.PSManagementPartner</span></span>

## <span data-ttu-id="2cfe0-124">Note</span><span class="sxs-lookup"><span data-stu-id="2cfe0-124">NOTES</span></span>

## <span data-ttu-id="2cfe0-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2cfe0-125">RELATED LINKS</span></span>

[<span data-ttu-id="2cfe0-126">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="2cfe0-126">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="2cfe0-127">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="2cfe0-127">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="2cfe0-128">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="2cfe0-128">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)
