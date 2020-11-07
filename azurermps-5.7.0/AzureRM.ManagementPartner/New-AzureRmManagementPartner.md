---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393044
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/New-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/New-AzureRmManagementPartner.md
ms.openlocfilehash: 9a6d6d0d21a38ac5ff41460021287e0701de6057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519432"
---
# <span data-ttu-id="6363b-101">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="6363b-101">New-AzureRmManagementPartner</span></span>

## <span data-ttu-id="6363b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6363b-102">SYNOPSIS</span></span>
<span data-ttu-id="6363b-103">Associa un ID Microsoft Partner Network (MPN) all'utente autenticato o all'entità di servizio corrente.</span><span class="sxs-lookup"><span data-stu-id="6363b-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6363b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6363b-104">SYNTAX</span></span>

```
New-AzureRmManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6363b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6363b-105">DESCRIPTION</span></span>
<span data-ttu-id="6363b-106">Associa un ID Microsoft Partner Network (MPN) all'utente autenticato o all'entità di servizio corrente.</span><span class="sxs-lookup"><span data-stu-id="6363b-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="6363b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6363b-107">EXAMPLES</span></span>

### <span data-ttu-id="6363b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6363b-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="6363b-109">Aggiungere un partner di gestione</span><span class="sxs-lookup"><span data-stu-id="6363b-109">Add a management partner</span></span> 

## <span data-ttu-id="6363b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6363b-110">PARAMETERS</span></span>

### <span data-ttu-id="6363b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6363b-111">-DefaultProfile</span></span>
<span data-ttu-id="6363b-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6363b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6363b-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="6363b-113">-PartnerId</span></span>
<span data-ttu-id="6363b-114">L'ID del partner di gestione è un numero a 6 cifre</span><span class="sxs-lookup"><span data-stu-id="6363b-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6363b-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6363b-115">-Confirm</span></span>
<span data-ttu-id="6363b-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6363b-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6363b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6363b-117">-WhatIf</span></span>
<span data-ttu-id="6363b-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6363b-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6363b-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6363b-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6363b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6363b-120">CommonParameters</span></span>
<span data-ttu-id="6363b-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6363b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6363b-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6363b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6363b-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6363b-123">INPUTS</span></span>

### <span data-ttu-id="6363b-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6363b-124">None</span></span>

## <span data-ttu-id="6363b-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6363b-125">OUTPUTS</span></span>

### <span data-ttu-id="6363b-126">Microsoft. Azure. Commands. resources. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="6363b-126">Microsoft.Azure.Commands.Resources.PSManagementPartner</span></span>

## <span data-ttu-id="6363b-127">Note</span><span class="sxs-lookup"><span data-stu-id="6363b-127">NOTES</span></span>

## <span data-ttu-id="6363b-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6363b-128">RELATED LINKS</span></span>

[<span data-ttu-id="6363b-129">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="6363b-129">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="6363b-130">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="6363b-130">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)

[<span data-ttu-id="6363b-131">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="6363b-131">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)