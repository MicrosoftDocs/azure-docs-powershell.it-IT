---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D927B159-AD68-4071-ADE3-FA2430750D72
online version: ''
schema: 2.0.0
ms.openlocfilehash: 001466cb00ad15f1cbfef6dcf9fd3ce9b931109b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029917"
---
# <span data-ttu-id="c43c1-101">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="c43c1-101">Remove-AzureStoreAddOn</span></span>

## <span data-ttu-id="c43c1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c43c1-102">SYNOPSIS</span></span>
<span data-ttu-id="c43c1-103">Rimuove un'istanza di componente aggiuntivo esistente.</span><span class="sxs-lookup"><span data-stu-id="c43c1-103">Removes an existing add-on instance.</span></span>

## <span data-ttu-id="c43c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c43c1-104">SYNTAX</span></span>

```
Remove-AzureStoreAddOn -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c43c1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c43c1-105">DESCRIPTION</span></span>
<span data-ttu-id="c43c1-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c43c1-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c43c1-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c43c1-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c43c1-108">Rimuove un'istanza del componente aggiuntivo esistente dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="c43c1-108">Removes an existing add-on instance from the current subscription.</span></span>

## <span data-ttu-id="c43c1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c43c1-109">EXAMPLES</span></span>

### <span data-ttu-id="c43c1-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c43c1-110">Example 1</span></span>
```
PS C:\> Remove-AzureStoreAddOn MyAddOn
```

<span data-ttu-id="c43c1-111">In questo esempio viene rimosso un componente aggiuntivo denominato AddOn dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="c43c1-111">This example removes an add-on named MyAddOn from the current subscription.</span></span>

## <span data-ttu-id="c43c1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c43c1-112">PARAMETERS</span></span>

### <span data-ttu-id="c43c1-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="c43c1-113">-Name</span></span>
<span data-ttu-id="c43c1-114">Specifica il nome dell'istanza del componente aggiuntivo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c43c1-114">Specifies the name of the add-on instance to remove.</span></span>

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

### <span data-ttu-id="c43c1-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c43c1-115">-PassThru</span></span>
<span data-ttu-id="c43c1-116">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="c43c1-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c43c1-117">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="c43c1-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c43c1-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="c43c1-118">-Profile</span></span>
<span data-ttu-id="c43c1-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c43c1-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c43c1-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c43c1-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c43c1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c43c1-121">CommonParameters</span></span>
<span data-ttu-id="c43c1-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c43c1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c43c1-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c43c1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c43c1-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c43c1-124">INPUTS</span></span>

## <span data-ttu-id="c43c1-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c43c1-125">OUTPUTS</span></span>

## <span data-ttu-id="c43c1-126">Note</span><span class="sxs-lookup"><span data-stu-id="c43c1-126">NOTES</span></span>

## <span data-ttu-id="c43c1-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c43c1-127">RELATED LINKS</span></span>

[<span data-ttu-id="c43c1-128">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="c43c1-128">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="c43c1-129">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="c43c1-129">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="c43c1-130">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="c43c1-130">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


