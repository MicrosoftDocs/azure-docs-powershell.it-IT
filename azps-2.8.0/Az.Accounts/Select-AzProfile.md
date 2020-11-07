---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
ms.openlocfilehash: 35b15fab6888a300fcef9f80b05aa034a9f07ce3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676187"
---
# <span data-ttu-id="00cc6-101">Select-AzProfile</span><span class="sxs-lookup"><span data-stu-id="00cc6-101">Select-AzProfile</span></span>

## <span data-ttu-id="00cc6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="00cc6-102">SYNOPSIS</span></span>
<span data-ttu-id="00cc6-103">Per i moduli che supportano più profili di servizio, caricare i cmdlet corrispondenti al profilo del servizio specifico.</span><span class="sxs-lookup"><span data-stu-id="00cc6-103">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="00cc6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00cc6-104">SYNTAX</span></span>

```
Select-AzProfile -Name <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00cc6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00cc6-105">DESCRIPTION</span></span>
<span data-ttu-id="00cc6-106">Per i moduli che supportano più profili di servizio, caricare i cmdlet corrispondenti al profilo del servizio specifico.</span><span class="sxs-lookup"><span data-stu-id="00cc6-106">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="00cc6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00cc6-107">EXAMPLES</span></span>

### <span data-ttu-id="00cc6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="00cc6-108">Example 1</span></span>
```powershell
PS C:\> Select-AzProfile hybrid-2019-03
```

<span data-ttu-id="00cc6-109">Caricare i cmdlet per il profilo AzureStack dal 2019 marzo</span><span class="sxs-lookup"><span data-stu-id="00cc6-109">Load cmdlets for the AzureStack profile from March 2019</span></span>

## <span data-ttu-id="00cc6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="00cc6-110">PARAMETERS</span></span>

### <span data-ttu-id="00cc6-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="00cc6-111">-Name</span></span>
<span data-ttu-id="00cc6-112">Nome del profilo da selezionare</span><span class="sxs-lookup"><span data-stu-id="00cc6-112">The name of the profile to select</span></span>

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

### <span data-ttu-id="00cc6-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00cc6-113">-PassThru</span></span>
<span data-ttu-id="00cc6-114">Quando è presente, forza il cmdlet a restituire un valore per l'esecuzione corretta</span><span class="sxs-lookup"><span data-stu-id="00cc6-114">When present, forces the cmdlet to return a value on successful execution</span></span>

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

### <span data-ttu-id="00cc6-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="00cc6-115">-Confirm</span></span>
<span data-ttu-id="00cc6-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00cc6-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00cc6-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00cc6-117">-WhatIf</span></span>
<span data-ttu-id="00cc6-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00cc6-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00cc6-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00cc6-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00cc6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00cc6-120">CommonParameters</span></span>
<span data-ttu-id="00cc6-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00cc6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00cc6-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00cc6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00cc6-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="00cc6-123">INPUTS</span></span>

### <span data-ttu-id="00cc6-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="00cc6-124">None</span></span>

## <span data-ttu-id="00cc6-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00cc6-125">OUTPUTS</span></span>

### <span data-ttu-id="00cc6-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="00cc6-126">System.Object</span></span>
## <span data-ttu-id="00cc6-127">Note</span><span class="sxs-lookup"><span data-stu-id="00cc6-127">NOTES</span></span>

## <span data-ttu-id="00cc6-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00cc6-128">RELATED LINKS</span></span>
