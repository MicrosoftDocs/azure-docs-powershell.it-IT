---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
ms.openlocfilehash: 796000ac20ab887d4abd26039da2a111a19141ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516980"
---
# <span data-ttu-id="1f6ff-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1f6ff-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="1f6ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f6ff-102">SYNOPSIS</span></span>
<span data-ttu-id="1f6ff-103">Rimuove un set di disponibilità da Azure.</span><span class="sxs-lookup"><span data-stu-id="1f6ff-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f6ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f6ff-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f6ff-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f6ff-105">DESCRIPTION</span></span>
<span data-ttu-id="1f6ff-106">Il cmdlet **Remove-AzureRmAvailabilitySet** rimuove un set di disponibilità da Azure.</span><span class="sxs-lookup"><span data-stu-id="1f6ff-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="1f6ff-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f6ff-107">EXAMPLES</span></span>

### <span data-ttu-id="1f6ff-108">Esempio 1: rimuovere un set di disponibilità</span><span class="sxs-lookup"><span data-stu-id="1f6ff-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="1f6ff-109">Questo comando rimuove un set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1f6ff-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="1f6ff-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f6ff-110">PARAMETERS</span></span>

### <span data-ttu-id="1f6ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f6ff-111">-DefaultProfile</span></span>
<span data-ttu-id="1f6ff-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f6ff-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f6ff-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1f6ff-113">-Force</span></span>
<span data-ttu-id="1f6ff-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1f6ff-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f6ff-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f6ff-115">-Name</span></span>
<span data-ttu-id="1f6ff-116">Nome del set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="1f6ff-116">The availability set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f6ff-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f6ff-117">-ResourceGroupName</span></span>
<span data-ttu-id="1f6ff-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1f6ff-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f6ff-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1f6ff-119">-Confirm</span></span>
<span data-ttu-id="1f6ff-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f6ff-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f6ff-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f6ff-121">-WhatIf</span></span>
<span data-ttu-id="1f6ff-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f6ff-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1f6ff-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f6ff-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f6ff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f6ff-124">CommonParameters</span></span>
<span data-ttu-id="1f6ff-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f6ff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f6ff-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f6ff-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f6ff-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f6ff-127">INPUTS</span></span>

## <span data-ttu-id="1f6ff-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f6ff-128">OUTPUTS</span></span>

## <span data-ttu-id="1f6ff-129">Note</span><span class="sxs-lookup"><span data-stu-id="1f6ff-129">NOTES</span></span>

## <span data-ttu-id="1f6ff-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f6ff-130">RELATED LINKS</span></span>

[<span data-ttu-id="1f6ff-131">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1f6ff-131">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="1f6ff-132">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1f6ff-132">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


