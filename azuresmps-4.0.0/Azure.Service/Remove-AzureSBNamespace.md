---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6E369BDF-AE3C-416B-81B7-097C20147CBE
online version: ''
schema: 2.0.0
ms.openlocfilehash: bb48f7412c957ceefb7df03d79e57ce8e75447d5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029592"
---
# <span data-ttu-id="4c145-101">Remove-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="4c145-101">Remove-AzureSBNamespace</span></span>

## <span data-ttu-id="4c145-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c145-102">SYNOPSIS</span></span>
<span data-ttu-id="4c145-103">Rimuove uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="4c145-103">Removes a namespace.</span></span>

## <span data-ttu-id="4c145-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c145-104">SYNTAX</span></span>

```
Remove-AzureSBNamespace -Name <String> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c145-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c145-105">DESCRIPTION</span></span>
<span data-ttu-id="4c145-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4c145-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4c145-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="4c145-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="4c145-108">Il cmdlet **Remove-AzureSBNamespace** rimuove uno spazio dei nomi del servizio per Service Bus.</span><span class="sxs-lookup"><span data-stu-id="4c145-108">The **Remove-AzureSBNamespace** cmdlet removes a service namespace for Service Bus.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="4c145-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c145-109">EXAMPLES</span></span>

## <span data-ttu-id="4c145-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c145-110">PARAMETERS</span></span>

### <span data-ttu-id="4c145-111">-Force</span><span class="sxs-lookup"><span data-stu-id="4c145-111">-Force</span></span>
<span data-ttu-id="4c145-112">Se abilitato, rimuove lo spazio dei nomi senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="4c145-112">If enabled, removes the namespace without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4c145-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c145-113">-Name</span></span>
<span data-ttu-id="4c145-114">Specifica il nome dello spazio dei nomi da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="4c145-114">Specifies the name of the namespace to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c145-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c145-115">-PassThru</span></span>
<span data-ttu-id="4c145-116">Fa sì che l'operazione restituisca true se riesce.</span><span class="sxs-lookup"><span data-stu-id="4c145-116">Causes the operation to return true if it succeeds.</span></span>

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

### <span data-ttu-id="4c145-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="4c145-117">-Profile</span></span>
<span data-ttu-id="4c145-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c145-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4c145-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="4c145-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c145-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4c145-120">-Confirm</span></span>
<span data-ttu-id="4c145-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c145-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c145-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c145-122">-WhatIf</span></span>
<span data-ttu-id="4c145-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c145-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c145-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c145-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c145-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c145-125">CommonParameters</span></span>
<span data-ttu-id="4c145-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c145-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c145-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c145-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c145-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c145-128">INPUTS</span></span>

## <span data-ttu-id="4c145-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c145-129">OUTPUTS</span></span>

## <span data-ttu-id="4c145-130">Note</span><span class="sxs-lookup"><span data-stu-id="4c145-130">NOTES</span></span>

## <span data-ttu-id="4c145-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c145-131">RELATED LINKS</span></span>

[<span data-ttu-id="4c145-132">New-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="4c145-132">New-AzureSBNamespace</span></span>](./New-AzureSBNamespace.md)


