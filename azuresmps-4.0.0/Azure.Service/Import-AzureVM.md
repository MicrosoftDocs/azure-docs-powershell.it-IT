---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7180CAC6-BFC1-4A18-A754-83D5F05C5BEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: c62c30558147bccd9cdecc73925b7e1a379d1c5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029717"
---
# <span data-ttu-id="d22a0-101">Import-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d22a0-101">Import-AzureVM</span></span>

## <span data-ttu-id="d22a0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d22a0-102">SYNOPSIS</span></span>
<span data-ttu-id="d22a0-103">Importa uno stato di una macchina virtuale Azure da un file.</span><span class="sxs-lookup"><span data-stu-id="d22a0-103">Imports an Azure virtual machine state from a file.</span></span>

## <span data-ttu-id="d22a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d22a0-104">SYNTAX</span></span>

```
Import-AzureVM [-Path] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="d22a0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d22a0-105">DESCRIPTION</span></span>
<span data-ttu-id="d22a0-106">Il cmdlet **Import-AzureVM** importa lo stato salvato in precedenza di una macchina virtuale da un file XML.</span><span class="sxs-lookup"><span data-stu-id="d22a0-106">The **Import-AzureVM** cmdlet imports the previously saved state of a virtual machine from an XML file.</span></span>
<span data-ttu-id="d22a0-107">Questo cmdlet è utile quando si vuole creare una macchina virtuale dai dati importati in un momento successivo.</span><span class="sxs-lookup"><span data-stu-id="d22a0-107">This cmdlet is useful when you want to subsequently create a virtual machine from the imported data.</span></span>

<span data-ttu-id="d22a0-108">L'esecuzione di **Export-AzureVM** , seguita da **Remove-AzureVM** e quindi **Import-AzureVM** per ricreare una macchina virtuale può far sì che la macchina virtuale risultante abbia un indirizzo IP diverso rispetto all'originale.</span><span class="sxs-lookup"><span data-stu-id="d22a0-108">Running **Export-AzureVM** , followed by **Remove-AzureVM** and then **Import-AzureVM** to recreate a virtual machine can cause the resultant virtual machine to have a different IP address than the original.</span></span>

## <span data-ttu-id="d22a0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d22a0-109">EXAMPLES</span></span>

### <span data-ttu-id="d22a0-110">Esempio 1: importare uno stato macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="d22a0-110">Example 1: Import a virtual machine state</span></span>
```
PS C:\> Import-AzureVM -Path "C:\VMstate.xml" | New-AzureVM -ServiceName "ContosoService02"
```

<span data-ttu-id="d22a0-111">Questo comando importa lo stato di una macchina virtuale dal file VMstate.xml e quindi crea una macchina virtuale nel servizio cloud specificato.</span><span class="sxs-lookup"><span data-stu-id="d22a0-111">This command imports the state of a virtual machine from the VMstate.xml file, and then creates a virtual machine in the specified cloud service.</span></span>

## <span data-ttu-id="d22a0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d22a0-112">PARAMETERS</span></span>

### <span data-ttu-id="d22a0-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d22a0-113">-InformationAction</span></span>
<span data-ttu-id="d22a0-114">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="d22a0-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d22a0-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d22a0-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d22a0-116">Continuare</span><span class="sxs-lookup"><span data-stu-id="d22a0-116">Continue</span></span>
- <span data-ttu-id="d22a0-117">Ignora</span><span class="sxs-lookup"><span data-stu-id="d22a0-117">Ignore</span></span>
- <span data-ttu-id="d22a0-118">Informarsi</span><span class="sxs-lookup"><span data-stu-id="d22a0-118">Inquire</span></span>
- <span data-ttu-id="d22a0-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d22a0-119">SilentlyContinue</span></span>
- <span data-ttu-id="d22a0-120">Stop</span><span class="sxs-lookup"><span data-stu-id="d22a0-120">Stop</span></span>
- <span data-ttu-id="d22a0-121">Sospensione</span><span class="sxs-lookup"><span data-stu-id="d22a0-121">Suspend</span></span>

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

### <span data-ttu-id="d22a0-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d22a0-122">-InformationVariable</span></span>
<span data-ttu-id="d22a0-123">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="d22a0-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d22a0-124">-Path</span><span class="sxs-lookup"><span data-stu-id="d22a0-124">-Path</span></span>
<span data-ttu-id="d22a0-125">Specifica il percorso del file con lo stato della macchina virtuale salvato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="d22a0-125">Specifies the path of the file with the previously saved virtual machine state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22a0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d22a0-126">CommonParameters</span></span>
<span data-ttu-id="d22a0-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d22a0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d22a0-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d22a0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d22a0-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d22a0-129">INPUTS</span></span>

## <span data-ttu-id="d22a0-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d22a0-130">OUTPUTS</span></span>

## <span data-ttu-id="d22a0-131">Note</span><span class="sxs-lookup"><span data-stu-id="d22a0-131">NOTES</span></span>

## <span data-ttu-id="d22a0-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d22a0-132">RELATED LINKS</span></span>

[<span data-ttu-id="d22a0-133">Export-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d22a0-133">Export-AzureVM</span></span>](./Export-AzureVM.md)

[<span data-ttu-id="d22a0-134">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d22a0-134">New-AzureVM</span></span>](./New-AzureVM.md)


