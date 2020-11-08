---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 78099E89-63C9-4019-A4ED-EF37D2383A09
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23e6165e50c227320875fa70e97d63b0cdd78781
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023635"
---
# <span data-ttu-id="226c6-101">Export-AzureVM</span><span class="sxs-lookup"><span data-stu-id="226c6-101">Export-AzureVM</span></span>

## <span data-ttu-id="226c6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="226c6-102">SYNOPSIS</span></span>
<span data-ttu-id="226c6-103">Esporta uno stato di una macchina virtuale di Azure in un file.</span><span class="sxs-lookup"><span data-stu-id="226c6-103">Exports an Azure virtual machine state to a file.</span></span>

## <span data-ttu-id="226c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="226c6-104">SYNTAX</span></span>

```
Export-AzureVM [-ServiceName] <String> [-Name] <String> [-Path] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="226c6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="226c6-105">DESCRIPTION</span></span>
<span data-ttu-id="226c6-106">Il cmdlet **Export-AzureVM** esporta lo stato di una macchina virtuale in un file XML.</span><span class="sxs-lookup"><span data-stu-id="226c6-106">The **Export-AzureVM** cmdlet exports the state of a virtual machine to an .xml file.</span></span>

<span data-ttu-id="226c6-107">L'esecuzione di **Export-AzureVM** , seguita da **Remove-AzureVM** e quindi **Import-AzureVM** per ricreare una macchina virtuale può far sì che la macchina virtuale risultante abbia un indirizzo IP diverso rispetto all'originale.</span><span class="sxs-lookup"><span data-stu-id="226c6-107">Running **Export-AzureVM** , followed by **Remove-AzureVM** and then **Import-AzureVM** to recreate a virtual machine can cause the resultant virtual machine to have a different IP address than the original.</span></span>

## <span data-ttu-id="226c6-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="226c6-108">EXAMPLES</span></span>

### <span data-ttu-id="226c6-109">Esempio 1: esportare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="226c6-109">Example 1: Export a virtual machine</span></span>
```
PS C:\> Export-AzureVM -ServiceName "ContosoService" -Name "ContosoRole06" -Path "C:\vms\VMstate.xml"
```

<span data-ttu-id="226c6-110">Questo comando Esporta lo stato della macchina virtuale specificata nel file VMstate.xml.</span><span class="sxs-lookup"><span data-stu-id="226c6-110">This command exports the state of the specified virtual machine to the VMstate.xml file.</span></span>

## <span data-ttu-id="226c6-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="226c6-111">PARAMETERS</span></span>

### <span data-ttu-id="226c6-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="226c6-112">-InformationAction</span></span>
<span data-ttu-id="226c6-113">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="226c6-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="226c6-114">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="226c6-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="226c6-115">Continuare</span><span class="sxs-lookup"><span data-stu-id="226c6-115">Continue</span></span>
- <span data-ttu-id="226c6-116">Ignora</span><span class="sxs-lookup"><span data-stu-id="226c6-116">Ignore</span></span>
- <span data-ttu-id="226c6-117">Informarsi</span><span class="sxs-lookup"><span data-stu-id="226c6-117">Inquire</span></span>
- <span data-ttu-id="226c6-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="226c6-118">SilentlyContinue</span></span>
- <span data-ttu-id="226c6-119">Stop</span><span class="sxs-lookup"><span data-stu-id="226c6-119">Stop</span></span>
- <span data-ttu-id="226c6-120">Sospensione</span><span class="sxs-lookup"><span data-stu-id="226c6-120">Suspend</span></span>

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

### <span data-ttu-id="226c6-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="226c6-121">-InformationVariable</span></span>
<span data-ttu-id="226c6-122">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="226c6-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="226c6-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="226c6-123">-Name</span></span>
<span data-ttu-id="226c6-124">Specifica il nome della macchina virtuale per cui questo cmdlet esporta lo stato.</span><span class="sxs-lookup"><span data-stu-id="226c6-124">Specifies the name of the virtual machine for which this cmdlet exports state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="226c6-125">-Path</span><span class="sxs-lookup"><span data-stu-id="226c6-125">-Path</span></span>
<span data-ttu-id="226c6-126">Specifica il percorso e il nome file a cui questo cmdlet salva lo stato della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="226c6-126">Specifies the path and file name to which this cmdlet saves the virtual machine state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="226c6-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="226c6-127">-Profile</span></span>
<span data-ttu-id="226c6-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="226c6-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="226c6-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="226c6-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="226c6-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="226c6-130">-ServiceName</span></span>
<span data-ttu-id="226c6-131">Specifica il nome del servizio Azure che ospita la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="226c6-131">Specifies the name of the Azure service that hosts the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="226c6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="226c6-132">CommonParameters</span></span>
<span data-ttu-id="226c6-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="226c6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="226c6-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="226c6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="226c6-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="226c6-135">INPUTS</span></span>

## <span data-ttu-id="226c6-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="226c6-136">OUTPUTS</span></span>

## <span data-ttu-id="226c6-137">Note</span><span class="sxs-lookup"><span data-stu-id="226c6-137">NOTES</span></span>

## <span data-ttu-id="226c6-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="226c6-138">RELATED LINKS</span></span>

[<span data-ttu-id="226c6-139">Import-AzureVM</span><span class="sxs-lookup"><span data-stu-id="226c6-139">Import-AzureVM</span></span>](./Import-AzureVM.md)


