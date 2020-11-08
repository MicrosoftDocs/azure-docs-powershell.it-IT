---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9AAEDD44-D11E-47A3-BF0F-D8445A018759
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46dbd7ec58cc112e6573fa3d9c6a52fe0ee14b33
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029905"
---
# <span data-ttu-id="bf386-101">Remove-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="bf386-101">Remove-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="bf386-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bf386-102">SYNOPSIS</span></span>
<span data-ttu-id="bf386-103">Rimuove l'estensione marionetta applicata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bf386-103">Removes the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="bf386-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bf386-104">SYNTAX</span></span>

```
Remove-AzureVMPuppetExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bf386-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf386-105">DESCRIPTION</span></span>
<span data-ttu-id="bf386-106">Il cmdlet **Remove-AzureVMPuppetExtension** rimuove l'estensione marionetta applicata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bf386-106">The **Remove-AzureVMPuppetExtension** cmdlet removes the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="bf386-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bf386-107">EXAMPLES</span></span>

### <span data-ttu-id="bf386-108">Esempio 1: rimuovere l'estensione marionetta applicata in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="bf386-108">Example 1: Remove the Puppet extension applied on a virtual machine</span></span>
```
PS C:\> Remove-AzureVMPuppetExtension -VM $VM;
```

<span data-ttu-id="bf386-109">Questo comando rimuove l'estensione marionetta applicata nella macchina virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="bf386-109">This command removes the Puppet extension applied on the specified virtual machine.</span></span>

## <span data-ttu-id="bf386-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bf386-110">PARAMETERS</span></span>

### <span data-ttu-id="bf386-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bf386-111">-InformationAction</span></span>
<span data-ttu-id="bf386-112">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="bf386-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bf386-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="bf386-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bf386-114">Continuare</span><span class="sxs-lookup"><span data-stu-id="bf386-114">Continue</span></span>
- <span data-ttu-id="bf386-115">Ignora</span><span class="sxs-lookup"><span data-stu-id="bf386-115">Ignore</span></span>
- <span data-ttu-id="bf386-116">Informarsi</span><span class="sxs-lookup"><span data-stu-id="bf386-116">Inquire</span></span>
- <span data-ttu-id="bf386-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bf386-117">SilentlyContinue</span></span>
- <span data-ttu-id="bf386-118">Stop</span><span class="sxs-lookup"><span data-stu-id="bf386-118">Stop</span></span>
- <span data-ttu-id="bf386-119">Sospensione</span><span class="sxs-lookup"><span data-stu-id="bf386-119">Suspend</span></span>

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

### <span data-ttu-id="bf386-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bf386-120">-InformationVariable</span></span>
<span data-ttu-id="bf386-121">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="bf386-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bf386-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="bf386-122">-Profile</span></span>
<span data-ttu-id="bf386-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf386-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bf386-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="bf386-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bf386-125">-VM</span><span class="sxs-lookup"><span data-stu-id="bf386-125">-VM</span></span>
<span data-ttu-id="bf386-126">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="bf386-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="bf386-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf386-127">CommonParameters</span></span>
<span data-ttu-id="bf386-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf386-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf386-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf386-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf386-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bf386-130">INPUTS</span></span>

## <span data-ttu-id="bf386-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bf386-131">OUTPUTS</span></span>

## <span data-ttu-id="bf386-132">Note</span><span class="sxs-lookup"><span data-stu-id="bf386-132">NOTES</span></span>

## <span data-ttu-id="bf386-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bf386-133">RELATED LINKS</span></span>

[<span data-ttu-id="bf386-134">Get-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="bf386-134">Get-AzureVMPuppetExtension</span></span>](./Get-AzureVMPuppetExtension.md)

[<span data-ttu-id="bf386-135">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="bf386-135">Set-AzureVMPuppetExtension</span></span>](./Set-AzureVMPuppetExtension.md)


