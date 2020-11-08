---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C19A1DC0-47FA-4687-B81F-315EA04AD4A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22591c1aa5a670e8f0d73f206ed6d2bcbe52c88f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023452"
---
# <span data-ttu-id="c4a64-101">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c4a64-101">Remove-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="c4a64-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4a64-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a64-103">Rimuove un'estensione di SQL Server di una macchina virtuale di Azure da un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c4a64-103">Removes an Azure virtual machine SQL Server extension from a virtual machine object.</span></span>

## <span data-ttu-id="c4a64-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4a64-104">SYNTAX</span></span>

```
Remove-AzureVMSqlServerExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c4a64-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4a64-105">DESCRIPTION</span></span>
<span data-ttu-id="c4a64-106">Il cmdlet **Remove-AzureVMSqlServerExtension** rimuove un'estensione di SQL Server di una macchina virtuale Azure da un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c4a64-106">The **Remove-AzureVMSqlServerExtension** cmdlet removes an Azure virtual machine SQL Server extension from a virtual machine object.</span></span>

## <span data-ttu-id="c4a64-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4a64-107">EXAMPLES</span></span>

### <span data-ttu-id="c4a64-108">1:</span><span class="sxs-lookup"><span data-stu-id="c4a64-108">1:</span></span>
```

```

## <span data-ttu-id="c4a64-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4a64-109">PARAMETERS</span></span>

### <span data-ttu-id="c4a64-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c4a64-110">-InformationAction</span></span>
<span data-ttu-id="c4a64-111">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="c4a64-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c4a64-112">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c4a64-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c4a64-113">Continuare</span><span class="sxs-lookup"><span data-stu-id="c4a64-113">Continue</span></span>
- <span data-ttu-id="c4a64-114">Ignora</span><span class="sxs-lookup"><span data-stu-id="c4a64-114">Ignore</span></span>
- <span data-ttu-id="c4a64-115">Informarsi</span><span class="sxs-lookup"><span data-stu-id="c4a64-115">Inquire</span></span>
- <span data-ttu-id="c4a64-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c4a64-116">SilentlyContinue</span></span>
- <span data-ttu-id="c4a64-117">Stop</span><span class="sxs-lookup"><span data-stu-id="c4a64-117">Stop</span></span>
- <span data-ttu-id="c4a64-118">Sospensione</span><span class="sxs-lookup"><span data-stu-id="c4a64-118">Suspend</span></span>

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

### <span data-ttu-id="c4a64-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c4a64-119">-InformationVariable</span></span>
<span data-ttu-id="c4a64-120">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="c4a64-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c4a64-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="c4a64-121">-Profile</span></span>
<span data-ttu-id="c4a64-122">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4a64-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c4a64-123">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c4a64-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c4a64-124">-VM</span><span class="sxs-lookup"><span data-stu-id="c4a64-124">-VM</span></span>
<span data-ttu-id="c4a64-125">Specifica l'oggetto macchina virtuale persistente da cui questo cmdlet rimuove l'estensione.</span><span class="sxs-lookup"><span data-stu-id="c4a64-125">Specifies the persistent virtual machine object that this cmdlet removes the extension from.</span></span>

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

### <span data-ttu-id="c4a64-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a64-126">CommonParameters</span></span>
<span data-ttu-id="c4a64-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4a64-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a64-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4a64-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a64-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4a64-129">INPUTS</span></span>

## <span data-ttu-id="c4a64-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4a64-130">OUTPUTS</span></span>

## <span data-ttu-id="c4a64-131">Note</span><span class="sxs-lookup"><span data-stu-id="c4a64-131">NOTES</span></span>

## <span data-ttu-id="c4a64-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4a64-132">RELATED LINKS</span></span>

[<span data-ttu-id="c4a64-133">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c4a64-133">Get-AzureVMSqlServerExtension</span></span>](./Get-AzureVMSqlServerExtension.md)

[<span data-ttu-id="c4a64-134">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c4a64-134">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


