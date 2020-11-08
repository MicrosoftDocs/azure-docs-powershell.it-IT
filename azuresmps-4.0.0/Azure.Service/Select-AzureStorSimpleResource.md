---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E771D1F2-A06B-44BB-AAFF-9459DC6303E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 273edfe08e4d2476cd4c1baa2967a829ec1bbcc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023406"
---
# <span data-ttu-id="672c0-101">Select-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="672c0-101">Select-AzureStorSimpleResource</span></span>

## <span data-ttu-id="672c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="672c0-102">SYNOPSIS</span></span>
<span data-ttu-id="672c0-103">Imposta una risorsa come risorsa corrente.</span><span class="sxs-lookup"><span data-stu-id="672c0-103">Sets a resource as the current resource.</span></span>

## <span data-ttu-id="672c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="672c0-104">SYNTAX</span></span>

```
Select-AzureStorSimpleResource -ResourceName <String> [-RegistrationKey <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="672c0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="672c0-105">DESCRIPTION</span></span>
<span data-ttu-id="672c0-106">Il cmdlet **Select-AzureStorSimpleResource** imposta una risorsa come risorsa corrente.</span><span class="sxs-lookup"><span data-stu-id="672c0-106">The **Select-AzureStorSimpleResource** cmdlet sets a resource as the current resource.</span></span>
<span data-ttu-id="672c0-107">Dopo aver selezionato una risorsa, gli altri cmdlet si applicano all'interno del contesto della risorsa.</span><span class="sxs-lookup"><span data-stu-id="672c0-107">After you select a resource, other cmdlets apply within that resource context.</span></span>

## <span data-ttu-id="672c0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="672c0-108">EXAMPLES</span></span>

### <span data-ttu-id="672c0-109">Esempio 1: selezionare una risorsa per la prima volta</span><span class="sxs-lookup"><span data-stu-id="672c0-109">Example 1: Select a resource for the first time</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa" -RegistrationKey "<your registration key>"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

<span data-ttu-id="672c0-110">Questo comando consente di selezionare la risorsa denominata Contoso64-Tsqa come contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="672c0-110">This command selects the resource named Contoso64-Tsqa as the current context.</span></span>
<span data-ttu-id="672c0-111">In questo esempio il computer non ha avuto questo contesto inizializzato in precedenza e, pertanto, devi specificare un valore per il parametro *RegistrationKey* .</span><span class="sxs-lookup"><span data-stu-id="672c0-111">In this example, the computer has not had this context initialized previously, and, therefore, you must specify a value for the *RegistrationKey* parameter.</span></span>

### <span data-ttu-id="672c0-112">Esempio 2: tentativo di selezione di una risorsa</span><span class="sxs-lookup"><span data-stu-id="672c0-112">Example 2: Attempt to select a resource</span></span>
```
This command gets the current context for this computer by using the **Get-AzureStorSimpleResourceContext** cmdlet. The current selected resource is Contoso64-Tsqa. This is consistent with the previous example. 
PS C:\>Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa 

This command attempts to reset the resource to be Contoso02-Resource. For this example, this resource has not been previously selected. The registration key is not saved or included in the command. The command cannot select the resource. 
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso02-Resource"
Select-AzureStorSimpleResource : Could not find the persisted secret. Please use Select-AzureStorSimpleResource and
provide the Registration key once again.
```

### <span data-ttu-id="672c0-113">Esempio 3: selezionare una risorsa selezionata in precedenza</span><span class="sxs-lookup"><span data-stu-id="672c0-113">Example 3: Select a previously selected resource</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

<span data-ttu-id="672c0-114">Questo comando consente di selezionare la risorsa denominata Contoso64-Tsqa come contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="672c0-114">This command selects the resource named Contoso64-Tsqa as the current context.</span></span>
<span data-ttu-id="672c0-115">In questo esempio, il contesto è stato selezionato in precedenza e, pertanto, non è necessario specificare un valore per il parametro *RegistrationKey* .</span><span class="sxs-lookup"><span data-stu-id="672c0-115">In this example, that context has previously been selected, and, therefore, you do not need to specify a value for the *RegistrationKey* parameter.</span></span>

## <span data-ttu-id="672c0-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="672c0-116">PARAMETERS</span></span>

### <span data-ttu-id="672c0-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="672c0-117">-Profile</span></span>
<span data-ttu-id="672c0-118">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="672c0-118">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="672c0-119">-RegistrationKey</span><span class="sxs-lookup"><span data-stu-id="672c0-119">-RegistrationKey</span></span>
<span data-ttu-id="672c0-120">Specifica una chiave di registrazione.</span><span class="sxs-lookup"><span data-stu-id="672c0-120">Specifies a registration key.</span></span>
<span data-ttu-id="672c0-121">Specificare una chiave per la prima volta che si seleziona una risorsa.</span><span class="sxs-lookup"><span data-stu-id="672c0-121">Specify a key the first time that you select a resource.</span></span>
<span data-ttu-id="672c0-122">Quando questo cmdlet seleziona la risorsa corrente, i cmdlet usano questa chiave, se necessario.</span><span class="sxs-lookup"><span data-stu-id="672c0-122">After this cmdlet selects the current resource, cmdlets use this key, as required.</span></span>
<span data-ttu-id="672c0-123">Per altre informazioni, vedere [ottenere la chiave di registrazione del servizio](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  ( https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) nella rete Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="672c0-123">For more information, see [Get the service registration key](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  (https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) on the Microsoft Developer Network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="672c0-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="672c0-124">-ResourceName</span></span>
<span data-ttu-id="672c0-125">Specifica il nome della risorsa da selezionare come risorsa corrente.</span><span class="sxs-lookup"><span data-stu-id="672c0-125">Specifies the name of the resource to select as the current resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="672c0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="672c0-126">CommonParameters</span></span>
<span data-ttu-id="672c0-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="672c0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="672c0-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="672c0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="672c0-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="672c0-129">INPUTS</span></span>

### <span data-ttu-id="672c0-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="672c0-130">None</span></span>

## <span data-ttu-id="672c0-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="672c0-131">OUTPUTS</span></span>

### <span data-ttu-id="672c0-132">StorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="672c0-132">StorSimpleResourceContext</span></span>
<span data-ttu-id="672c0-133">Questo cmdlet restituisce un oggetto **StorSimpleResourceContext** che contiene dettagli per il contesto della risorsa.</span><span class="sxs-lookup"><span data-stu-id="672c0-133">This cmdlet returns a **StorSimpleResourceContext** object that contains details for the resource context.</span></span>

## <span data-ttu-id="672c0-134">Note</span><span class="sxs-lookup"><span data-stu-id="672c0-134">NOTES</span></span>

## <span data-ttu-id="672c0-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="672c0-135">RELATED LINKS</span></span>

[<span data-ttu-id="672c0-136">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="672c0-136">Get-AzureStorSimpleResource</span></span>](./Get-AzureStorSimpleResource.md)

[<span data-ttu-id="672c0-137">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="672c0-137">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)


