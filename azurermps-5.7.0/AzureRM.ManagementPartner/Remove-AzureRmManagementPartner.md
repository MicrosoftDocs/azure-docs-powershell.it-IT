---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393045
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Remove-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Remove-AzureRmManagementPartner.md
ms.openlocfilehash: 703c38d02ef6a6a339c58c861961cd2ad92ecb7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518983"
---
# <span data-ttu-id="619d3-101">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="619d3-101">Remove-AzureRmManagementPartner</span></span>

## <span data-ttu-id="619d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="619d3-102">SYNOPSIS</span></span>
<span data-ttu-id="619d3-103">Eliminare l'ID Microsoft Partner Network (MPN) dell'utente o dell'entità di servizio corrente autenticato.</span><span class="sxs-lookup"><span data-stu-id="619d3-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="619d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="619d3-104">SYNTAX</span></span>

```
Remove-AzureRmManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="619d3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="619d3-105">DESCRIPTION</span></span>
<span data-ttu-id="619d3-106">Eliminare l'ID Microsoft Partner Network (MPN) dell'utente o dell'entità di servizio corrente autenticato.</span><span class="sxs-lookup"><span data-stu-id="619d3-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="619d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="619d3-107">EXAMPLES</span></span>

### <span data-ttu-id="619d3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="619d3-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzureRmManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="619d3-109">Rimuovi partner di gestione</span><span class="sxs-lookup"><span data-stu-id="619d3-109">Remove management partner</span></span> 

## <span data-ttu-id="619d3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="619d3-110">PARAMETERS</span></span>

### <span data-ttu-id="619d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="619d3-111">-DefaultProfile</span></span>
<span data-ttu-id="619d3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="619d3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="619d3-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="619d3-113">-PartnerId</span></span>
<span data-ttu-id="619d3-114">L'ID del partner di gestione è un numero a 6 cifre</span><span class="sxs-lookup"><span data-stu-id="619d3-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="619d3-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="619d3-115">-PassThru</span></span>
<span data-ttu-id="619d3-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="619d3-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="619d3-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="619d3-117">-Confirm</span></span>
<span data-ttu-id="619d3-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="619d3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="619d3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="619d3-119">-WhatIf</span></span>
<span data-ttu-id="619d3-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="619d3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="619d3-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="619d3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="619d3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="619d3-122">CommonParameters</span></span>
<span data-ttu-id="619d3-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="619d3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="619d3-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="619d3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="619d3-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="619d3-125">INPUTS</span></span>

### <span data-ttu-id="619d3-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="619d3-126">None</span></span>

## <span data-ttu-id="619d3-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="619d3-127">OUTPUTS</span></span>

### <span data-ttu-id="619d3-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="619d3-128">System.Object</span></span>

## <span data-ttu-id="619d3-129">Note</span><span class="sxs-lookup"><span data-stu-id="619d3-129">NOTES</span></span>

## <span data-ttu-id="619d3-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="619d3-130">RELATED LINKS</span></span>

[<span data-ttu-id="619d3-131">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="619d3-131">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="619d3-132">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="619d3-132">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)

[<span data-ttu-id="619d3-133">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="619d3-133">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)
