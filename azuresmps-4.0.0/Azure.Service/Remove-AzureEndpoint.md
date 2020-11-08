---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5A068EC9-3745-4219-BA03-C56CB9D9D157
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24fad9fc499c3f7abec5e7539fd1e221835849ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029940"
---
# <span data-ttu-id="f14d1-101">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="f14d1-101">Remove-AzureEndpoint</span></span>

## <span data-ttu-id="f14d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f14d1-102">SYNOPSIS</span></span>
<span data-ttu-id="f14d1-103">Elimina un endpoint da una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="f14d1-103">Deletes an endpoint from an Azure virtual machine.</span></span>

## <span data-ttu-id="f14d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f14d1-104">SYNTAX</span></span>

```
Remove-AzureEndpoint [-Name] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f14d1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f14d1-105">DESCRIPTION</span></span>
<span data-ttu-id="f14d1-106">Il cmdlet **Remove-AzureEndpoint** Elimina un endpoint da un oggetto macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="f14d1-106">The **Remove-AzureEndpoint** cmdlet deletes an endpoint from an Azure virtual machine object.</span></span>

## <span data-ttu-id="f14d1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f14d1-107">EXAMPLES</span></span>

### <span data-ttu-id="f14d1-108">Esempio 1: rimuovere un endpoint</span><span class="sxs-lookup"><span data-stu-id="f14d1-108">Example 1: Remove an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine01" | Remove-AzureEndpoint -Name "HttpIn" | Update-AzureVM
```

<span data-ttu-id="f14d1-109">Questo comando Recupera la configurazione di una macchina virtuale denominata VirtualMachine01 usando il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="f14d1-109">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="f14d1-110">Il comando lo passa al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="f14d1-110">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f14d1-111">Questo cmdlet consente di rimuovere un endpoint denominato Httpin.</span><span class="sxs-lookup"><span data-stu-id="f14d1-111">This cmdlet removes an endpoint named HttpIn.</span></span>
<span data-ttu-id="f14d1-112">Il comando passa l'oggetto macchina virtuale al cmdlet **Update-AzureVM** , che implementa le modifiche.</span><span class="sxs-lookup"><span data-stu-id="f14d1-112">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="f14d1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f14d1-113">PARAMETERS</span></span>

### <span data-ttu-id="f14d1-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f14d1-114">-InformationAction</span></span>
<span data-ttu-id="f14d1-115">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="f14d1-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f14d1-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f14d1-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f14d1-117">Continuare</span><span class="sxs-lookup"><span data-stu-id="f14d1-117">Continue</span></span>
- <span data-ttu-id="f14d1-118">Ignora</span><span class="sxs-lookup"><span data-stu-id="f14d1-118">Ignore</span></span>
- <span data-ttu-id="f14d1-119">Informarsi</span><span class="sxs-lookup"><span data-stu-id="f14d1-119">Inquire</span></span>
- <span data-ttu-id="f14d1-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f14d1-120">SilentlyContinue</span></span>
- <span data-ttu-id="f14d1-121">Stop</span><span class="sxs-lookup"><span data-stu-id="f14d1-121">Stop</span></span>
- <span data-ttu-id="f14d1-122">Sospensione</span><span class="sxs-lookup"><span data-stu-id="f14d1-122">Suspend</span></span>

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

### <span data-ttu-id="f14d1-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f14d1-123">-InformationVariable</span></span>
<span data-ttu-id="f14d1-124">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="f14d1-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f14d1-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f14d1-125">-Name</span></span>
<span data-ttu-id="f14d1-126">Specifica il nome dell'endpoint eliminato dal cmdlet dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f14d1-126">Specifies the name of the endpoint that this cmdlet deletes from the virtual machine.</span></span>

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

### <span data-ttu-id="f14d1-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="f14d1-127">-Profile</span></span>
<span data-ttu-id="f14d1-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f14d1-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f14d1-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="f14d1-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f14d1-130">-VM</span><span class="sxs-lookup"><span data-stu-id="f14d1-130">-VM</span></span>
<span data-ttu-id="f14d1-131">Specifica la macchina virtuale da cui questo cmdlet elimina un endpoint.</span><span class="sxs-lookup"><span data-stu-id="f14d1-131">Specifies the virtual machine from which this cmdlet deletes an endpoint.</span></span>

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

### <span data-ttu-id="f14d1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f14d1-132">CommonParameters</span></span>
<span data-ttu-id="f14d1-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f14d1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f14d1-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f14d1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f14d1-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f14d1-135">INPUTS</span></span>

## <span data-ttu-id="f14d1-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f14d1-136">OUTPUTS</span></span>

## <span data-ttu-id="f14d1-137">Note</span><span class="sxs-lookup"><span data-stu-id="f14d1-137">NOTES</span></span>

## <span data-ttu-id="f14d1-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f14d1-138">RELATED LINKS</span></span>

[<span data-ttu-id="f14d1-139">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="f14d1-139">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="f14d1-140">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="f14d1-140">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="f14d1-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f14d1-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="f14d1-142">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="f14d1-142">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="f14d1-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f14d1-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


