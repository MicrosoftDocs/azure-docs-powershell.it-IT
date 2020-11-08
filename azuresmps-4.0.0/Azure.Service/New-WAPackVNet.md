---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CB2936E4-E403-44B3-9CB8-617308E54C50
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9059e5bad8441f25846cf98a12c5e8dada2e814a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030859"
---
# <span data-ttu-id="2cd8c-101">New-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="2cd8c-101">New-WAPackVNet</span></span>

## <span data-ttu-id="2cd8c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2cd8c-102">SYNOPSIS</span></span>
<span data-ttu-id="2cd8c-103">Crea una rete virtualizzata.</span><span class="sxs-lookup"><span data-stu-id="2cd8c-103">Creates a virtualized network.</span></span>

## <span data-ttu-id="2cd8c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2cd8c-104">SYNTAX</span></span>

```
New-WAPackVNet -LogicalNetwork <LogicalNetwork> -Name <String> [-Description <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2cd8c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2cd8c-105">DESCRIPTION</span></span>
<span data-ttu-id="2cd8c-106">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="2cd8c-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="2cd8c-107">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2cd8c-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2cd8c-108">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2cd8c-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2cd8c-109">Il cmdlet **New-WAPackVNet** crea una rete virtualizzata.</span><span class="sxs-lookup"><span data-stu-id="2cd8c-109">The **New-WAPackVNet** cmdlet creates a virtualized network.</span></span>

## <span data-ttu-id="2cd8c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2cd8c-110">EXAMPLES</span></span>

### <span data-ttu-id="2cd8c-111">Esempio 1: creare una rete virtualizzata</span><span class="sxs-lookup"><span data-stu-id="2cd8c-111">Example 1: Create a virtualized network</span></span>
```
PS C:\> $LogicalNetwork = Get-WAPackLogicalNetwork -Name "ContosoLogicalNetwork01"
PS C:\> New-WAPackVNet -LogicalNetwork $LogicalNetwork -Name "ContosoVNett01" -Description "A description"
```

<span data-ttu-id="2cd8c-112">Il primo comando recupera prima di tutto la rete logica a cui si vuole aggiungere una nuova rete virtualizzata.</span><span class="sxs-lookup"><span data-stu-id="2cd8c-112">The first command first retrieves the logical network to which we want to add a new virtualized network.</span></span>
<span data-ttu-id="2cd8c-113">Questa rete logica è denominata ContosoLogicalNetwork01.</span><span class="sxs-lookup"><span data-stu-id="2cd8c-113">This logical network is named ContosoLogicalNetwork01.</span></span>

<span data-ttu-id="2cd8c-114">Il secondo e l'ultimo comando crea una rete virtualizzata usando la rete logica recuperata in precedenza, un nome (ContosoVNett01) e una descrizione (una descrizione).</span><span class="sxs-lookup"><span data-stu-id="2cd8c-114">The second and last command creates a virtualized network using the previously retrieved logical network, a name (ContosoVNett01) and a description (A description).</span></span>

## <span data-ttu-id="2cd8c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2cd8c-115">PARAMETERS</span></span>

### <span data-ttu-id="2cd8c-116">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="2cd8c-116">-Description</span></span>
<span data-ttu-id="2cd8c-117">Specifica una descrizione per la rete virtualizzata.</span><span class="sxs-lookup"><span data-stu-id="2cd8c-117">Specifies a description for the virtualized network.</span></span>

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

### <span data-ttu-id="2cd8c-118">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="2cd8c-118">-LogicalNetwork</span></span>
<span data-ttu-id="2cd8c-119">Specifica un LogicalNetwork associato alla rete virtualizzata.</span><span class="sxs-lookup"><span data-stu-id="2cd8c-119">Specifies a LogicalNetwork associated with the virtualized network.</span></span>

```yaml
Type: LogicalNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd8c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="2cd8c-120">-Name</span></span>
<span data-ttu-id="2cd8c-121">Specifica un nome per la rete virtualizzata.</span><span class="sxs-lookup"><span data-stu-id="2cd8c-121">Specifies a name for the virtualized network.</span></span>

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

### <span data-ttu-id="2cd8c-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="2cd8c-122">-Profile</span></span>
<span data-ttu-id="2cd8c-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cd8c-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2cd8c-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="2cd8c-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2cd8c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cd8c-125">CommonParameters</span></span>
<span data-ttu-id="2cd8c-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cd8c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cd8c-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cd8c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cd8c-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2cd8c-128">INPUTS</span></span>

## <span data-ttu-id="2cd8c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2cd8c-129">OUTPUTS</span></span>

## <span data-ttu-id="2cd8c-130">Note</span><span class="sxs-lookup"><span data-stu-id="2cd8c-130">NOTES</span></span>

## <span data-ttu-id="2cd8c-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2cd8c-131">RELATED LINKS</span></span>

[<span data-ttu-id="2cd8c-132">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="2cd8c-132">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="2cd8c-133">Remove-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="2cd8c-133">Remove-WAPackVNet</span></span>](./Remove-WAPackVNet.md)


