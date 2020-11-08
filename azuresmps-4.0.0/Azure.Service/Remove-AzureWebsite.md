---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8062D57E-8381-4715-9AA8-551F15DCC492
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2627bdb2f098d5b09851ec5970dd2a73840d24e6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023441"
---
# <span data-ttu-id="77205-101">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="77205-101">Remove-AzureWebsite</span></span>

## <span data-ttu-id="77205-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77205-102">SYNOPSIS</span></span>
<span data-ttu-id="77205-103">Rimuove il sito Web specificato da Azure.</span><span class="sxs-lookup"><span data-stu-id="77205-103">Removes the specified website from Azure.</span></span>

## <span data-ttu-id="77205-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77205-104">SYNTAX</span></span>

```
Remove-AzureWebsite [-Force] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77205-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77205-105">DESCRIPTION</span></span>
<span data-ttu-id="77205-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="77205-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="77205-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="77205-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="77205-108">Il cmdlet **Remove-AzureWebsite** rimuove il sito Web specificato da Azure, con o senza una richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="77205-108">The **Remove-AzureWebsite** cmdlet removes the specified website from Azure, either with or without a prompt for confirmation.</span></span>

## <span data-ttu-id="77205-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77205-109">EXAMPLES</span></span>

### <span data-ttu-id="77205-110">Esempio 1: rimuovere il sito Web corrente</span><span class="sxs-lookup"><span data-stu-id="77205-110">Example 1: Remove the current website</span></span>
```
PS C:\> Remove-AzureWebsite
```

<span data-ttu-id="77205-111">Questo esempio rimuove il sito Web in Azure associato alla directory corrente.</span><span class="sxs-lookup"><span data-stu-id="77205-111">This example removes the website in Azure associated with the current directory.</span></span>

### <span data-ttu-id="77205-112">Esempio 2: rimuovere un sito Web senza conferma</span><span class="sxs-lookup"><span data-stu-id="77205-112">Example 2: Remove a website without confirmation</span></span>
```
PS C:\> Remove-AzureWebsite -Name mySite -Force
```

<span data-ttu-id="77205-113">In questo esempio viene eliminato il sito Web denominato sito personale senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="77205-113">This example deletes the website named mySite without prompting for confirmation.</span></span>

## <span data-ttu-id="77205-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77205-114">PARAMETERS</span></span>

### <span data-ttu-id="77205-115">-Force</span><span class="sxs-lookup"><span data-stu-id="77205-115">-Force</span></span>
<span data-ttu-id="77205-116">Se specificato, Elimina il sito Web specificato senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="77205-116">If specified, deletes the specified website without prompting for confirmation.</span></span>

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

### <span data-ttu-id="77205-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="77205-117">-Name</span></span>
<span data-ttu-id="77205-118">Specifica il nome del sito Web da eliminare.</span><span class="sxs-lookup"><span data-stu-id="77205-118">Specifies the name of the website to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77205-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="77205-119">-Profile</span></span>
<span data-ttu-id="77205-120">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77205-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="77205-121">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="77205-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="77205-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="77205-122">-Slot</span></span>
<span data-ttu-id="77205-123">Specifica il nome dello slot del sito Web.</span><span class="sxs-lookup"><span data-stu-id="77205-123">Specifies the slot name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77205-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="77205-124">-Confirm</span></span>
<span data-ttu-id="77205-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77205-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77205-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77205-126">-WhatIf</span></span>
<span data-ttu-id="77205-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77205-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77205-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77205-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77205-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77205-129">CommonParameters</span></span>
<span data-ttu-id="77205-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77205-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77205-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77205-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77205-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77205-132">INPUTS</span></span>

## <span data-ttu-id="77205-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77205-133">OUTPUTS</span></span>

## <span data-ttu-id="77205-134">Note</span><span class="sxs-lookup"><span data-stu-id="77205-134">NOTES</span></span>

## <span data-ttu-id="77205-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77205-135">RELATED LINKS</span></span>

[<span data-ttu-id="77205-136">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="77205-136">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)


