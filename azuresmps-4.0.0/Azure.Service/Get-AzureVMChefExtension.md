---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1721107D-22FF-4A42-93C6-FD812DF81C33
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac1bb63645b8db9e6a66971ad4ecd3b545a39100
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030007"
---
# <span data-ttu-id="5aa3f-101">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="5aa3f-101">Get-AzureVMChefExtension</span></span>

## <span data-ttu-id="5aa3f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5aa3f-102">SYNOPSIS</span></span>
<span data-ttu-id="5aa3f-103">Ottiene l'estensione dello chef applicata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-103">Gets the Chef extension applied on a virtual machine.</span></span>

## <span data-ttu-id="5aa3f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5aa3f-104">SYNTAX</span></span>

```
Get-AzureVMChefExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5aa3f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5aa3f-105">DESCRIPTION</span></span>
<span data-ttu-id="5aa3f-106">Il cmdlet **Get-AzureVMChefExtension** Ottiene l'estensione chef applicata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-106">The **Get-AzureVMChefExtension** cmdlet gets the Chef extension applied on a virtual machine.</span></span>

## <span data-ttu-id="5aa3f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5aa3f-107">EXAMPLES</span></span>

### <span data-ttu-id="5aa3f-108">Esempio 1: ottenere l'estensione dello chef applicata nella macchina virtuale specificata</span><span class="sxs-lookup"><span data-stu-id="5aa3f-108">Example 1: Get the Chef extension applied on the specified virtual machine</span></span>
```
PS C:\> Get-AzureVMChefExtension -VM $VM;
```

<span data-ttu-id="5aa3f-109">Questo comando consente di ottenere l'estensione chef applicata nella macchina virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-109">This command gets the Chef extension applied on the specified virtual machine.</span></span>

## <span data-ttu-id="5aa3f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5aa3f-110">PARAMETERS</span></span>

### <span data-ttu-id="5aa3f-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5aa3f-111">-InformationAction</span></span>
<span data-ttu-id="5aa3f-112">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5aa3f-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5aa3f-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5aa3f-114">Continuare</span><span class="sxs-lookup"><span data-stu-id="5aa3f-114">Continue</span></span>
- <span data-ttu-id="5aa3f-115">Ignora</span><span class="sxs-lookup"><span data-stu-id="5aa3f-115">Ignore</span></span>
- <span data-ttu-id="5aa3f-116">Informarsi</span><span class="sxs-lookup"><span data-stu-id="5aa3f-116">Inquire</span></span>
- <span data-ttu-id="5aa3f-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5aa3f-117">SilentlyContinue</span></span>
- <span data-ttu-id="5aa3f-118">Stop</span><span class="sxs-lookup"><span data-stu-id="5aa3f-118">Stop</span></span>
- <span data-ttu-id="5aa3f-119">Sospensione</span><span class="sxs-lookup"><span data-stu-id="5aa3f-119">Suspend</span></span>

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

### <span data-ttu-id="5aa3f-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5aa3f-120">-InformationVariable</span></span>
<span data-ttu-id="5aa3f-121">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5aa3f-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="5aa3f-122">-Profile</span></span>
<span data-ttu-id="5aa3f-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5aa3f-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5aa3f-125">-VM</span><span class="sxs-lookup"><span data-stu-id="5aa3f-125">-VM</span></span>
<span data-ttu-id="5aa3f-126">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="5aa3f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aa3f-127">CommonParameters</span></span>
<span data-ttu-id="5aa3f-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aa3f-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5aa3f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aa3f-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5aa3f-130">INPUTS</span></span>

## <span data-ttu-id="5aa3f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5aa3f-131">OUTPUTS</span></span>

## <span data-ttu-id="5aa3f-132">Note</span><span class="sxs-lookup"><span data-stu-id="5aa3f-132">NOTES</span></span>

## <span data-ttu-id="5aa3f-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5aa3f-133">RELATED LINKS</span></span>

[<span data-ttu-id="5aa3f-134">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="5aa3f-134">Remove-AzureVMChefExtension</span></span>](./Remove-AzureVMChefExtension.md)

[<span data-ttu-id="5aa3f-135">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="5aa3f-135">Set-AzureVMChefExtension</span></span>](./Set-AzureVMChefExtension.md)


