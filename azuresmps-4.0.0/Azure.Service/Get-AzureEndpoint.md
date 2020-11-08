---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1CFB90FD-7BC5-4687-8D08-775097DDA062
online version: ''
schema: 2.0.0
ms.openlocfilehash: 651b38a21dff03ce3c5925040d65bc2967eeaa77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023603"
---
# <span data-ttu-id="1128a-101">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="1128a-101">Get-AzureEndpoint</span></span>

## <span data-ttu-id="1128a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1128a-102">SYNOPSIS</span></span>
<span data-ttu-id="1128a-103">Ottiene informazioni sugli endpoint assegnati a una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="1128a-103">Gets information about the endpoints that are assigned to an Azure virtual machine.</span></span>

## <span data-ttu-id="1128a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1128a-104">SYNTAX</span></span>

```
Get-AzureEndpoint [[-Name] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1128a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1128a-105">DESCRIPTION</span></span>
<span data-ttu-id="1128a-106">Il cmdlet **Get-AzureEndpoint** ottiene le informazioni sugli endpoint assegnati a una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="1128a-106">The **Get-AzureEndpoint** cmdlet gets information about the endpoints that are assigned to an Azure virtual machine.</span></span>

## <span data-ttu-id="1128a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1128a-107">EXAMPLES</span></span>

### <span data-ttu-id="1128a-108">Esempio 1: recuperare le informazioni sull'endpoint per una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="1128a-108">Example 1: Get endpoint information for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine12" | Get-AzureEndpoint
```

<span data-ttu-id="1128a-109">Questo comando Recupera la configurazione di una macchina virtuale denominata VirtualMachine12 usando il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="1128a-109">This command retrieves the configuration of a virtual machine named VirtualMachine12 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="1128a-110">Il comando lo passa al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="1128a-110">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1128a-111">Questo cmdlet ottiene le informazioni sull'endpoint per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1128a-111">This cmdlet gets endpoint information for that virtual machine.</span></span>

## <span data-ttu-id="1128a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1128a-112">PARAMETERS</span></span>

### <span data-ttu-id="1128a-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1128a-113">-InformationAction</span></span>
<span data-ttu-id="1128a-114">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="1128a-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1128a-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1128a-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1128a-116">Continuare</span><span class="sxs-lookup"><span data-stu-id="1128a-116">Continue</span></span>
- <span data-ttu-id="1128a-117">Ignora</span><span class="sxs-lookup"><span data-stu-id="1128a-117">Ignore</span></span>
- <span data-ttu-id="1128a-118">Informarsi</span><span class="sxs-lookup"><span data-stu-id="1128a-118">Inquire</span></span>
- <span data-ttu-id="1128a-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1128a-119">SilentlyContinue</span></span>
- <span data-ttu-id="1128a-120">Stop</span><span class="sxs-lookup"><span data-stu-id="1128a-120">Stop</span></span>
- <span data-ttu-id="1128a-121">Sospensione</span><span class="sxs-lookup"><span data-stu-id="1128a-121">Suspend</span></span>

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

### <span data-ttu-id="1128a-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1128a-122">-InformationVariable</span></span>
<span data-ttu-id="1128a-123">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="1128a-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1128a-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="1128a-124">-Name</span></span>
<span data-ttu-id="1128a-125">Specifica il nome dell'endpoint per cui questo cmdlet ottiene le informazioni.</span><span class="sxs-lookup"><span data-stu-id="1128a-125">Specifies the name of the endpoint for which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1128a-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="1128a-126">-Profile</span></span>
<span data-ttu-id="1128a-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1128a-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1128a-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="1128a-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1128a-129">-VM</span><span class="sxs-lookup"><span data-stu-id="1128a-129">-VM</span></span>
<span data-ttu-id="1128a-130">Specifica la macchina virtuale da cui questo cmdlet ottiene le informazioni sull'endpoint.</span><span class="sxs-lookup"><span data-stu-id="1128a-130">Specifies the virtual machine from which this cmdlet gets endpoint information.</span></span>

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

### <span data-ttu-id="1128a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1128a-131">CommonParameters</span></span>
<span data-ttu-id="1128a-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1128a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1128a-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1128a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1128a-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1128a-134">INPUTS</span></span>

## <span data-ttu-id="1128a-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1128a-135">OUTPUTS</span></span>

## <span data-ttu-id="1128a-136">Note</span><span class="sxs-lookup"><span data-stu-id="1128a-136">NOTES</span></span>

## <span data-ttu-id="1128a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1128a-137">RELATED LINKS</span></span>

[<span data-ttu-id="1128a-138">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="1128a-138">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="1128a-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="1128a-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="1128a-140">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="1128a-140">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="1128a-141">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="1128a-141">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)


