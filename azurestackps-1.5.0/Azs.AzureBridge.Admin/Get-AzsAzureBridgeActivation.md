---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 811a69b8d18c5e723702f73873188961f2739360
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/22/2020
ms.locfileid: "93522201"
---
# <span data-ttu-id="dcea9-101">Get-AzsAzureBridgeActivation</span><span class="sxs-lookup"><span data-stu-id="dcea9-101">Get-AzsAzureBridgeActivation</span></span>

## <span data-ttu-id="dcea9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dcea9-102">SYNOPSIS</span></span>
<span data-ttu-id="dcea9-103">Restituisce l'attivazione di Azure Bridge.</span><span class="sxs-lookup"><span data-stu-id="dcea9-103">Returns the Azure Bridge Activation.</span></span>

## <span data-ttu-id="dcea9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dcea9-104">SYNTAX</span></span>

### <span data-ttu-id="dcea9-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dcea9-105">List (Default)</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="dcea9-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="dcea9-106">Get</span></span>
```
Get-AzsAzureBridgeActivation -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="dcea9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcea9-107">ResourceId</span></span>
```
Get-AzsAzureBridgeActivation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="dcea9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dcea9-108">DESCRIPTION</span></span>
<span data-ttu-id="dcea9-109">Una volta registrata la pila di Azure, l'oggetto di attivazione contiene informazioni che collegano una distribuzione di Azure stack alla relativa registrazione in Azure, ad esempio la data di scadenza della registrazione, il nome e così via.</span><span class="sxs-lookup"><span data-stu-id="dcea9-109">Once Azure Stack has been registered, the activation object contains information that links an Azure Stack deployment to its registration in Azure, for example, the registration expiration date, name, etc.</span></span>

## <span data-ttu-id="dcea9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dcea9-110">EXAMPLES</span></span>

### <span data-ttu-id="dcea9-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="dcea9-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName 'activationRG'
```

<span data-ttu-id="dcea9-112">Ottenere un elenco delle attivazioni di Azure Bridge nel gruppo risorse "activationRG"</span><span class="sxs-lookup"><span data-stu-id="dcea9-112">Get a list of Azure Bridge Activations under the resource group "activationRG"</span></span>

### <span data-ttu-id="dcea9-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="dcea9-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -Name 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="dcea9-114">Ottenere un'attivazione di Azure Bridge per nome "attivazione" situata in "activationRG"</span><span class="sxs-lookup"><span data-stu-id="dcea9-114">Get an Azure Bridge Activation by name 'myActivation' situated under 'activationRG'</span></span>

## <span data-ttu-id="dcea9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dcea9-115">PARAMETERS</span></span>

### <span data-ttu-id="dcea9-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="dcea9-116">-Name</span></span>
<span data-ttu-id="dcea9-117">Nome dell'attivazione.</span><span class="sxs-lookup"><span data-stu-id="dcea9-117">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcea9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcea9-118">-ResourceGroupName</span></span>
<span data-ttu-id="dcea9-119">Gruppo di risorse usato durante la registrazione di Azure stack; è anche possibile visualizzare i nomi dei gruppi di risorse nel portale.</span><span class="sxs-lookup"><span data-stu-id="dcea9-119">The Resource Group used during the registration of Azure Stack; you can also view Resource Group names in the portal.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcea9-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcea9-120">-ResourceId</span></span>
<span data-ttu-id="dcea9-121">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="dcea9-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcea9-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="dcea9-122">-Skip</span></span>
<span data-ttu-id="dcea9-123">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="dcea9-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcea9-124">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="dcea9-124">-Top</span></span>
<span data-ttu-id="dcea9-125">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="dcea9-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="dcea9-126">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="dcea9-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcea9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcea9-127">CommonParameters</span></span>
<span data-ttu-id="dcea9-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcea9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcea9-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcea9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcea9-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dcea9-130">INPUTS</span></span>

## <span data-ttu-id="dcea9-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dcea9-131">OUTPUTS</span></span>

### <span data-ttu-id="dcea9-132">Microsoft. AzureStack. Management. AzureBridge. admin. Models. ActivationResource</span><span class="sxs-lookup"><span data-stu-id="dcea9-132">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ActivationResource</span></span>

## <span data-ttu-id="dcea9-133">Note</span><span class="sxs-lookup"><span data-stu-id="dcea9-133">NOTES</span></span>

## <span data-ttu-id="dcea9-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dcea9-134">RELATED LINKS</span></span>
