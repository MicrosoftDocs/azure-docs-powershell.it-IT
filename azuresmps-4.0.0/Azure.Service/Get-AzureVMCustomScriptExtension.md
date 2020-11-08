---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: DBB8EC31-877C-4DB1-8197-CA7A4148AE06
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f8767c9477db41251eb4732a2eb96d8dd782c20
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023489"
---
# <span data-ttu-id="cfe26-101">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="cfe26-101">Get-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="cfe26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cfe26-102">SYNOPSIS</span></span>
<span data-ttu-id="cfe26-103">Ottiene le informazioni da un'estensione di script personalizzata di Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="cfe26-103">Gets information from an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="cfe26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cfe26-104">SYNTAX</span></span>

```
Get-AzureVMCustomScriptExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cfe26-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cfe26-105">DESCRIPTION</span></span>
<span data-ttu-id="cfe26-106">Il cmdlet **Get-AzureVMCustomScriptExtension** ottiene le informazioni da un'estensione di script personalizzata di Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="cfe26-106">The **Get-AzureVMCustomScriptExtension** cmdlet gets information from an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="cfe26-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cfe26-107">EXAMPLES</span></span>

### <span data-ttu-id="cfe26-108">Esempio 1: ottenere un'estensione di script di una macchina virtuale Azure</span><span class="sxs-lookup"><span data-stu-id="cfe26-108">Example 1: Get an Azure virtual machine script extension</span></span>
```
PS C:\> Get-AzureVMCustomScriptExtension -VM $VM;
```

<span data-ttu-id="cfe26-109">Questo comando consente di ottenere un'estensione di script di una macchina virtuale Azure archiviata nella variabile $VM.</span><span class="sxs-lookup"><span data-stu-id="cfe26-109">This command gets an Azure virtual machine script extension stored in the variable $VM.</span></span>

## <span data-ttu-id="cfe26-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cfe26-110">PARAMETERS</span></span>

### <span data-ttu-id="cfe26-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="cfe26-111">-InformationAction</span></span>
<span data-ttu-id="cfe26-112">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="cfe26-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cfe26-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="cfe26-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cfe26-114">Continuare</span><span class="sxs-lookup"><span data-stu-id="cfe26-114">Continue</span></span>
- <span data-ttu-id="cfe26-115">Ignora</span><span class="sxs-lookup"><span data-stu-id="cfe26-115">Ignore</span></span>
- <span data-ttu-id="cfe26-116">Informarsi</span><span class="sxs-lookup"><span data-stu-id="cfe26-116">Inquire</span></span>
- <span data-ttu-id="cfe26-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cfe26-117">SilentlyContinue</span></span>
- <span data-ttu-id="cfe26-118">Stop</span><span class="sxs-lookup"><span data-stu-id="cfe26-118">Stop</span></span>
- <span data-ttu-id="cfe26-119">Sospensione</span><span class="sxs-lookup"><span data-stu-id="cfe26-119">Suspend</span></span>

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

### <span data-ttu-id="cfe26-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cfe26-120">-InformationVariable</span></span>
<span data-ttu-id="cfe26-121">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="cfe26-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cfe26-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="cfe26-122">-Profile</span></span>
<span data-ttu-id="cfe26-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfe26-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cfe26-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="cfe26-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cfe26-125">-VM</span><span class="sxs-lookup"><span data-stu-id="cfe26-125">-VM</span></span>
<span data-ttu-id="cfe26-126">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="cfe26-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="cfe26-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe26-127">CommonParameters</span></span>
<span data-ttu-id="cfe26-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfe26-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfe26-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfe26-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe26-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cfe26-130">INPUTS</span></span>

## <span data-ttu-id="cfe26-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cfe26-131">OUTPUTS</span></span>

## <span data-ttu-id="cfe26-132">Note</span><span class="sxs-lookup"><span data-stu-id="cfe26-132">NOTES</span></span>

## <span data-ttu-id="cfe26-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cfe26-133">RELATED LINKS</span></span>

[<span data-ttu-id="cfe26-134">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="cfe26-134">Remove-AzureVMCustomScriptExtension</span></span>](./Remove-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="cfe26-135">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="cfe26-135">Set-AzureVMCustomScriptExtension</span></span>](./Set-AzureVMCustomScriptExtension.md)


