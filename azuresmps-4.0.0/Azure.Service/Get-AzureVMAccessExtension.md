---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 734C98C1-0EF7-43E5-AB6F-A1C625FF9CE7
online version: ''
schema: 2.0.0
ms.openlocfilehash: f9713c8b39fa4e2842cdf1cfcbfe962ead86d729
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023493"
---
# <span data-ttu-id="bf32c-101">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="bf32c-101">Get-AzureVMAccessExtension</span></span>

## <span data-ttu-id="bf32c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bf32c-102">SYNOPSIS</span></span>
<span data-ttu-id="bf32c-103">Ottiene l'estensione VMAccess applicata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bf32c-103">Gets the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="bf32c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bf32c-104">SYNTAX</span></span>

```
Get-AzureVMAccessExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bf32c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf32c-105">DESCRIPTION</span></span>
<span data-ttu-id="bf32c-106">Il cmdlet **Get-AzureVMAccessExtension** Ottiene l'estensione VMAccess applicata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bf32c-106">The **Get-AzureVMAccessExtension** cmdlet gets the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="bf32c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bf32c-107">EXAMPLES</span></span>

### <span data-ttu-id="bf32c-108">Esempio 1: ottenere l'estensione VMAccess per una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="bf32c-108">Example 1: Get the VMAccess extension for a virtual machine</span></span>
```
PS C:\> Get-AzureVMAccessExtension -VM $VM;
```

<span data-ttu-id="bf32c-109">Questo comando ottiene l'estensione VMAccess per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bf32c-109">This command gets the VMAccess extension for a virtual machine.</span></span>

## <span data-ttu-id="bf32c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bf32c-110">PARAMETERS</span></span>

### <span data-ttu-id="bf32c-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bf32c-111">-InformationAction</span></span>
<span data-ttu-id="bf32c-112">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="bf32c-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bf32c-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="bf32c-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bf32c-114">Continuare</span><span class="sxs-lookup"><span data-stu-id="bf32c-114">Continue</span></span>
- <span data-ttu-id="bf32c-115">Ignora</span><span class="sxs-lookup"><span data-stu-id="bf32c-115">Ignore</span></span>
- <span data-ttu-id="bf32c-116">Informarsi</span><span class="sxs-lookup"><span data-stu-id="bf32c-116">Inquire</span></span>
- <span data-ttu-id="bf32c-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bf32c-117">SilentlyContinue</span></span>
- <span data-ttu-id="bf32c-118">Stop</span><span class="sxs-lookup"><span data-stu-id="bf32c-118">Stop</span></span>
- <span data-ttu-id="bf32c-119">Sospensione</span><span class="sxs-lookup"><span data-stu-id="bf32c-119">Suspend</span></span>

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

### <span data-ttu-id="bf32c-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bf32c-120">-InformationVariable</span></span>
<span data-ttu-id="bf32c-121">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="bf32c-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bf32c-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="bf32c-122">-Profile</span></span>
<span data-ttu-id="bf32c-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf32c-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bf32c-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="bf32c-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bf32c-125">-VM</span><span class="sxs-lookup"><span data-stu-id="bf32c-125">-VM</span></span>
<span data-ttu-id="bf32c-126">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="bf32c-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="bf32c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf32c-127">CommonParameters</span></span>
<span data-ttu-id="bf32c-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf32c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf32c-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf32c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf32c-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bf32c-130">INPUTS</span></span>

## <span data-ttu-id="bf32c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bf32c-131">OUTPUTS</span></span>

## <span data-ttu-id="bf32c-132">Note</span><span class="sxs-lookup"><span data-stu-id="bf32c-132">NOTES</span></span>

## <span data-ttu-id="bf32c-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bf32c-133">RELATED LINKS</span></span>

[<span data-ttu-id="bf32c-134">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="bf32c-134">Remove-AzureVMAccessExtension</span></span>](./Remove-AzureVMAccessExtension.md)

[<span data-ttu-id="bf32c-135">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="bf32c-135">Set-AzureVMAccessExtension</span></span>](./Set-AzureVMAccessExtension.md)


