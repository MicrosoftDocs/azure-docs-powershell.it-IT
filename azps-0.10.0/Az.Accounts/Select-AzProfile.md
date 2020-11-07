---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Select-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Select-AzProfile.md
ms.openlocfilehash: 04b98f15def219c269bf18f21fb371822cc97f6d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860166"
---
# <span data-ttu-id="27836-101">Select-AzProfile</span><span class="sxs-lookup"><span data-stu-id="27836-101">Select-AzProfile</span></span>

## <span data-ttu-id="27836-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27836-102">SYNOPSIS</span></span>
<span data-ttu-id="27836-103">Per i moduli che supportano più profili di servizio, caricare i cmdlet corrispondenti al profilo del servizio specifico.</span><span class="sxs-lookup"><span data-stu-id="27836-103">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="27836-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27836-104">SYNTAX</span></span>

```
Select-AzProfile -Name <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27836-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27836-105">DESCRIPTION</span></span>
<span data-ttu-id="27836-106">Per i moduli che supportano più profili di servizio, caricare i cmdlet corrispondenti al profilo del servizio specifico.</span><span class="sxs-lookup"><span data-stu-id="27836-106">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="27836-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27836-107">EXAMPLES</span></span>

### <span data-ttu-id="27836-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="27836-108">Example 1</span></span>
```powershell
PS C:\> Select-AzProfile hybrid-2019-03
```

<span data-ttu-id="27836-109">Caricare i cmdlet per il profilo AzureStack dal 2019 marzo</span><span class="sxs-lookup"><span data-stu-id="27836-109">Load cmdlets for the AzureStack profile from March 2019</span></span>

## <span data-ttu-id="27836-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27836-110">PARAMETERS</span></span>

### <span data-ttu-id="27836-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="27836-111">-Name</span></span>
<span data-ttu-id="27836-112">Nome del profilo da selezionare</span><span class="sxs-lookup"><span data-stu-id="27836-112">The name of the profile to select</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProfileName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27836-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27836-113">-PassThru</span></span>
<span data-ttu-id="27836-114">Quando è presente, forza il cmdlet a restituire un valore per l'esecuzione corretta</span><span class="sxs-lookup"><span data-stu-id="27836-114">When present, forces the cmdlet to return a value on successful execution</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27836-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="27836-115">-Confirm</span></span>
<span data-ttu-id="27836-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27836-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27836-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27836-117">-WhatIf</span></span>
<span data-ttu-id="27836-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27836-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27836-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27836-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27836-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27836-120">CommonParameters</span></span>
<span data-ttu-id="27836-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27836-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27836-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27836-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27836-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27836-123">INPUTS</span></span>

### <span data-ttu-id="27836-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="27836-124">None</span></span>

## <span data-ttu-id="27836-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27836-125">OUTPUTS</span></span>

### <span data-ttu-id="27836-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="27836-126">System.Object</span></span>
## <span data-ttu-id="27836-127">Note</span><span class="sxs-lookup"><span data-stu-id="27836-127">NOTES</span></span>

## <span data-ttu-id="27836-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27836-128">RELATED LINKS</span></span>
