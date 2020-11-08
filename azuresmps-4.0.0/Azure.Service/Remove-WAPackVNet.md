---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 42042533-9F84-4189-8C9F-01FD62F89DC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: db14b17e42d23e481468f563768b606d8baa2802
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030868"
---
# <span data-ttu-id="59e11-101">Remove-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="59e11-101">Remove-WAPackVNet</span></span>

## <span data-ttu-id="59e11-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59e11-102">SYNOPSIS</span></span>
<span data-ttu-id="59e11-103">Rimuove gli oggetti di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="59e11-103">Removes virtual network objects.</span></span>

## <span data-ttu-id="59e11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59e11-104">SYNTAX</span></span>

```
Remove-WAPackVNet -VNet <VMNetwork> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="59e11-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59e11-105">DESCRIPTION</span></span>
<span data-ttu-id="59e11-106">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="59e11-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="59e11-107">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="59e11-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="59e11-108">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="59e11-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="59e11-109">Il cmdlet **Remove-WAPackVNet** rimuove gli oggetti di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="59e11-109">The **Remove-WAPackVNet** cmdlet removes virtual network objects.</span></span>

## <span data-ttu-id="59e11-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59e11-110">EXAMPLES</span></span>

### <span data-ttu-id="59e11-111">Esempio 1: rimuovere una rete virtualizzata</span><span class="sxs-lookup"><span data-stu-id="59e11-111">Example 1: Remove a virtualized network</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Remove-WAPackVM -VNet $VNet
```

<span data-ttu-id="59e11-112">Il primo comando consente di ottenere la rete virtualizzata denominata ContosoVNet01 usando il cmdlet **Get-WAPackVNet** e quindi di archiviare tale oggetto nella variabile $VNet.</span><span class="sxs-lookup"><span data-stu-id="59e11-112">The first command gets the virtualized network named ContosoVNet01 by using the **Get-WAPackVNet** cmdlet, and then stores that object in the $VNet variable.</span></span>
<span data-ttu-id="59e11-113">Il secondo comando rimuove la rete virtualizzata archiviata in $VNet.</span><span class="sxs-lookup"><span data-stu-id="59e11-113">The second command removes the virtualized network stored in $VNet.</span></span>
<span data-ttu-id="59e11-114">Il comando richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="59e11-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="59e11-115">Esempio 2: rimuovere una rete virtualizzata senza conferma</span><span class="sxs-lookup"><span data-stu-id="59e11-115">Example 2: Remove a virtualized network without confirmation</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet02"
PS C:\> Remove-WAPackVNet -VNet $VNet -Force
```

<span data-ttu-id="59e11-116">Il primo comando ottiene il servizio cloud denominato ContosoVNet02 usando il cmdlet **Get-WAPackVNet** e quindi archivia tale oggetto nella variabile $VNet.</span><span class="sxs-lookup"><span data-stu-id="59e11-116">The first command gets the cloud service named ContosoVNet02 by using the **Get-WAPackVNet** cmdlet, and then stores that object in the $VNet variable.</span></span>
<span data-ttu-id="59e11-117">Il secondo comando rimuove la rete virtualizzata archiviata in $VNet.</span><span class="sxs-lookup"><span data-stu-id="59e11-117">The second command removes the virtualized network stored in $VNet.</span></span>
<span data-ttu-id="59e11-118">Questo comando include il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="59e11-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="59e11-119">Il comando non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="59e11-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="59e11-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59e11-120">PARAMETERS</span></span>

### <span data-ttu-id="59e11-121">-Force</span><span class="sxs-lookup"><span data-stu-id="59e11-121">-Force</span></span>
<span data-ttu-id="59e11-122">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="59e11-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="59e11-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59e11-123">-PassThru</span></span>
<span data-ttu-id="59e11-124">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="59e11-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="59e11-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="59e11-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="59e11-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="59e11-126">-Profile</span></span>
<span data-ttu-id="59e11-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59e11-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="59e11-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="59e11-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="59e11-129">-VNet</span><span class="sxs-lookup"><span data-stu-id="59e11-129">-VNet</span></span>
<span data-ttu-id="59e11-130">Specifica una rete virtualizzata.</span><span class="sxs-lookup"><span data-stu-id="59e11-130">Specifies a virtualized network.</span></span>
<span data-ttu-id="59e11-131">Per ottenere una rete virtualizzata, usare il cmdlet **Get-WAPackVNet** .</span><span class="sxs-lookup"><span data-stu-id="59e11-131">To obtain a virtualized network, use the **Get-WAPackVNet** cmdlet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59e11-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59e11-132">CommonParameters</span></span>
<span data-ttu-id="59e11-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59e11-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59e11-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59e11-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59e11-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59e11-135">INPUTS</span></span>

## <span data-ttu-id="59e11-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59e11-136">OUTPUTS</span></span>

## <span data-ttu-id="59e11-137">Note</span><span class="sxs-lookup"><span data-stu-id="59e11-137">NOTES</span></span>

## <span data-ttu-id="59e11-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59e11-138">RELATED LINKS</span></span>

[<span data-ttu-id="59e11-139">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="59e11-139">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="59e11-140">New-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="59e11-140">New-WAPackVNet</span></span>](./New-WAPackVNet.md)


