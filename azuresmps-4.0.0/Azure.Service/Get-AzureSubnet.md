---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 73CEA6A8-46C9-4772-9A67-03F532696CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c1287b3a0bb1cc39dea78fb4e92d2dcc4508c6a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023501"
---
# <span data-ttu-id="86679-101">Get-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="86679-101">Get-AzureSubnet</span></span>

## <span data-ttu-id="86679-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86679-102">SYNOPSIS</span></span>
<span data-ttu-id="86679-103">Ottiene un elenco di subnet associate alla macchina virtuale di Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="86679-103">Gets a list of subnets associated with the specified Azure virtual machine.</span></span>

## <span data-ttu-id="86679-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86679-104">SYNTAX</span></span>

```
Get-AzureSubnet -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="86679-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86679-105">DESCRIPTION</span></span>
<span data-ttu-id="86679-106">Il cmdlet **Get-AzureSubnet** restituisce un elenco delle subnet associate alla macchina virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="86679-106">The **Get-AzureSubnet** cmdlet returns a list the subnets associated with the specified virtual machine.</span></span>
<span data-ttu-id="86679-107">USA **Get-AzureVM** per specificare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="86679-107">Use **Get-AzureVM** to specify the virtual machine.</span></span>

## <span data-ttu-id="86679-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86679-108">EXAMPLES</span></span>

### <span data-ttu-id="86679-109">Esempio 1: ottenere subnet per una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="86679-109">Example 1: Get subnets for a virtual machine</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine01"
C:\PS> Get-AzureSubnet -VM $VM
```

<span data-ttu-id="86679-110">Il primo comando consente di ottenere una macchina virtuale denominata VirtualMachine01 nel servizio denominato ContosoService03 e quindi di archiviarla nella variabile $VM.</span><span class="sxs-lookup"><span data-stu-id="86679-110">The first command gets a virtual machine named VirtualMachine01 in the service named ContosoService03, and then stores it in the $VM variable.</span></span>

<span data-ttu-id="86679-111">Il secondo comando consente di ottenere le subnet di Azure per la macchina virtuale in $VM.</span><span class="sxs-lookup"><span data-stu-id="86679-111">The second command gets the Azure subnets for the virtual machine in $VM.</span></span>

## <span data-ttu-id="86679-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86679-112">PARAMETERS</span></span>

### <span data-ttu-id="86679-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="86679-113">-InformationAction</span></span>
<span data-ttu-id="86679-114">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="86679-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="86679-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="86679-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="86679-116">Continuare</span><span class="sxs-lookup"><span data-stu-id="86679-116">Continue</span></span>
- <span data-ttu-id="86679-117">Ignora</span><span class="sxs-lookup"><span data-stu-id="86679-117">Ignore</span></span>
- <span data-ttu-id="86679-118">Informarsi</span><span class="sxs-lookup"><span data-stu-id="86679-118">Inquire</span></span>
- <span data-ttu-id="86679-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="86679-119">SilentlyContinue</span></span>
- <span data-ttu-id="86679-120">Stop</span><span class="sxs-lookup"><span data-stu-id="86679-120">Stop</span></span>
- <span data-ttu-id="86679-121">Sospensione</span><span class="sxs-lookup"><span data-stu-id="86679-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86679-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="86679-122">-InformationVariable</span></span>
<span data-ttu-id="86679-123">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="86679-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86679-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="86679-124">-Profile</span></span>
<span data-ttu-id="86679-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86679-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="86679-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="86679-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="86679-127">-VM</span><span class="sxs-lookup"><span data-stu-id="86679-127">-VM</span></span>
<span data-ttu-id="86679-128">Specifica l'oggetto macchina virtuale da cui ottenere l'elenco subnet.</span><span class="sxs-lookup"><span data-stu-id="86679-128">Specifies the virtual machine object from which to get the subnet list.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86679-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86679-129">CommonParameters</span></span>
<span data-ttu-id="86679-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86679-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86679-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86679-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86679-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86679-132">INPUTS</span></span>

## <span data-ttu-id="86679-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86679-133">OUTPUTS</span></span>

## <span data-ttu-id="86679-134">Note</span><span class="sxs-lookup"><span data-stu-id="86679-134">NOTES</span></span>

## <span data-ttu-id="86679-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86679-135">RELATED LINKS</span></span>

[<span data-ttu-id="86679-136">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="86679-136">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="86679-137">Set-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="86679-137">Set-AzureSubnet</span></span>](./Set-AzureSubnet.md)


