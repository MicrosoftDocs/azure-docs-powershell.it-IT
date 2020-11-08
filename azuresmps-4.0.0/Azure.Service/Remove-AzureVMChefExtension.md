---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A46832F2-CA94-43A4-AFF9-70D02851713F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1146cee245693c19b333af5a4efd9fcc1bebc725
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023463"
---
# <span data-ttu-id="b645b-101">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="b645b-101">Remove-AzureVMChefExtension</span></span>

## <span data-ttu-id="b645b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b645b-102">SYNOPSIS</span></span>
<span data-ttu-id="b645b-103">Rimuove l'estensione chef applicata alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b645b-103">Removes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="b645b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b645b-104">SYNTAX</span></span>

```
Remove-AzureVMChefExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b645b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b645b-105">DESCRIPTION</span></span>
<span data-ttu-id="b645b-106">Il cmdlet **Remove-AzureVMChefExtension** Elimina l'estensione chef applicata alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b645b-106">The **Remove-AzureVMChefExtension** cmdlet deletes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="b645b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b645b-107">EXAMPLES</span></span>

### <span data-ttu-id="b645b-108">Esempio 1: rimuovere l'estensione dello chef applicata nella macchina virtuale specificata</span><span class="sxs-lookup"><span data-stu-id="b645b-108">Example 1: Remove the Chef extension applied on the specified virtual machine</span></span>
```
PS C:\> Remove-AzureVMChefExtension -VM $VM;
```

<span data-ttu-id="b645b-109">Questo comando rimuove l'estensione chef applicata alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b645b-109">This command removes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="b645b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b645b-110">PARAMETERS</span></span>

### <span data-ttu-id="b645b-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b645b-111">-InformationAction</span></span>
<span data-ttu-id="b645b-112">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="b645b-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b645b-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b645b-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b645b-114">Continuare</span><span class="sxs-lookup"><span data-stu-id="b645b-114">Continue</span></span>
- <span data-ttu-id="b645b-115">Ignora</span><span class="sxs-lookup"><span data-stu-id="b645b-115">Ignore</span></span>
- <span data-ttu-id="b645b-116">Informarsi</span><span class="sxs-lookup"><span data-stu-id="b645b-116">Inquire</span></span>
- <span data-ttu-id="b645b-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b645b-117">SilentlyContinue</span></span>
- <span data-ttu-id="b645b-118">Stop</span><span class="sxs-lookup"><span data-stu-id="b645b-118">Stop</span></span>
- <span data-ttu-id="b645b-119">Sospensione</span><span class="sxs-lookup"><span data-stu-id="b645b-119">Suspend</span></span>

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

### <span data-ttu-id="b645b-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b645b-120">-InformationVariable</span></span>
<span data-ttu-id="b645b-121">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="b645b-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b645b-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="b645b-122">-Profile</span></span>
<span data-ttu-id="b645b-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b645b-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b645b-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="b645b-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b645b-125">-VM</span><span class="sxs-lookup"><span data-stu-id="b645b-125">-VM</span></span>
<span data-ttu-id="b645b-126">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="b645b-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="b645b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b645b-127">CommonParameters</span></span>
<span data-ttu-id="b645b-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b645b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b645b-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b645b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b645b-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b645b-130">INPUTS</span></span>

## <span data-ttu-id="b645b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b645b-131">OUTPUTS</span></span>

## <span data-ttu-id="b645b-132">Note</span><span class="sxs-lookup"><span data-stu-id="b645b-132">NOTES</span></span>

## <span data-ttu-id="b645b-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b645b-133">RELATED LINKS</span></span>

[<span data-ttu-id="b645b-134">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="b645b-134">Get-AzureVMChefExtension</span></span>](./Get-AzureVMChefExtension.md)

[<span data-ttu-id="b645b-135">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="b645b-135">Set-AzureVMChefExtension</span></span>](./Set-AzureVMChefExtension.md)


