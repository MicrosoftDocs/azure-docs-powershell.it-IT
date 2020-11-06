---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393054
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Update-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Update-AzureRmManagementPartner.md
ms.openlocfilehash: 420353d7a8af1046456138918092ca56d5c6ed96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516516"
---
# <span data-ttu-id="d49c8-101">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="d49c8-101">Update-AzureRmManagementPartner</span></span>

## <span data-ttu-id="d49c8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d49c8-102">SYNOPSIS</span></span>
<span data-ttu-id="d49c8-103">Aggiorna l'ID Microsoft Partner Network (MPN) dell'utente o dell'entità di servizio corrente autenticato.</span><span class="sxs-lookup"><span data-stu-id="d49c8-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d49c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d49c8-104">SYNTAX</span></span>

```
Update-AzureRmManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d49c8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d49c8-105">DESCRIPTION</span></span>
<span data-ttu-id="d49c8-106">Aggiorna l'ID Microsoft Partner Network (MPN) dell'utente o dell'entità di servizio corrente autenticato.</span><span class="sxs-lookup"><span data-stu-id="d49c8-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="d49c8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d49c8-107">EXAMPLES</span></span>

### <span data-ttu-id="d49c8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d49c8-108">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="d49c8-109">Aggiornare il partner di gestione in uno nuovo</span><span class="sxs-lookup"><span data-stu-id="d49c8-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="d49c8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d49c8-110">PARAMETERS</span></span>

### <span data-ttu-id="d49c8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d49c8-111">-DefaultProfile</span></span>
<span data-ttu-id="d49c8-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d49c8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d49c8-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="d49c8-113">-PartnerId</span></span>
<span data-ttu-id="d49c8-114">L'ID del partner di gestione è un numero a 6 cifre</span><span class="sxs-lookup"><span data-stu-id="d49c8-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="d49c8-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d49c8-115">-Confirm</span></span>
<span data-ttu-id="d49c8-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d49c8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d49c8-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d49c8-117">-WhatIf</span></span>
<span data-ttu-id="d49c8-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d49c8-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d49c8-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d49c8-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d49c8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d49c8-120">CommonParameters</span></span>
<span data-ttu-id="d49c8-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d49c8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d49c8-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d49c8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d49c8-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d49c8-123">INPUTS</span></span>

### <span data-ttu-id="d49c8-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d49c8-124">None</span></span>

## <span data-ttu-id="d49c8-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d49c8-125">OUTPUTS</span></span>

### <span data-ttu-id="d49c8-126">Microsoft. Azure. Commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="d49c8-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="d49c8-127">Note</span><span class="sxs-lookup"><span data-stu-id="d49c8-127">NOTES</span></span>

## <span data-ttu-id="d49c8-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d49c8-128">RELATED LINKS</span></span>

[<span data-ttu-id="d49c8-129">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="d49c8-129">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="d49c8-130">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="d49c8-130">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="d49c8-131">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="d49c8-131">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)
