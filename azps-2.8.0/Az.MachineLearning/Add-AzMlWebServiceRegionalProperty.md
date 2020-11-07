---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: 877ef93dbecf3510887a24cb0b5dfe65948658f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673950"
---
# <span data-ttu-id="ad837-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="ad837-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="ad837-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad837-102">SYNOPSIS</span></span>
<span data-ttu-id="ad837-103">Crea proprietà del servizio Web regionali.</span><span class="sxs-lookup"><span data-stu-id="ad837-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="ad837-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad837-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad837-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad837-105">DESCRIPTION</span></span>
<span data-ttu-id="ad837-106">Crea le proprietà locali di Azure Machine Learning per un servizio Web esistente.</span><span class="sxs-lookup"><span data-stu-id="ad837-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="ad837-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad837-107">EXAMPLES</span></span>

### <span data-ttu-id="ad837-108">Esempio 1: aggiungere nuove proprietà regionali per gli Stati Uniti del centro ovest</span><span class="sxs-lookup"><span data-stu-id="ad837-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="ad837-109">Questo comando di esempio crea una proprietà Region per un servizio Web nell'area "West Central US".</span><span class="sxs-lookup"><span data-stu-id="ad837-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="ad837-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad837-110">PARAMETERS</span></span>

### <span data-ttu-id="ad837-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad837-111">-DefaultProfile</span></span>
<span data-ttu-id="ad837-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ad837-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad837-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ad837-113">-Force</span></span>
<span data-ttu-id="ad837-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ad837-114">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad837-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad837-115">-Name</span></span>
<span data-ttu-id="ad837-116">Nome del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="ad837-116">The name for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad837-117">-Area geografica</span><span class="sxs-lookup"><span data-stu-id="ad837-117">-Region</span></span>
<span data-ttu-id="ad837-118">Area geografica in cui creare le proprietà del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="ad837-118">The region in which to create the web service properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad837-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad837-119">-ResourceGroupName</span></span>
<span data-ttu-id="ad837-120">Gruppo di risorse in cui appartiene il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="ad837-120">The resource group in which the web service belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad837-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ad837-121">-Confirm</span></span>
<span data-ttu-id="ad837-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad837-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad837-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad837-123">-WhatIf</span></span>
<span data-ttu-id="ad837-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad837-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad837-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad837-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad837-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad837-126">CommonParameters</span></span>
<span data-ttu-id="ad837-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad837-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad837-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad837-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad837-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad837-129">INPUTS</span></span>

### <span data-ttu-id="ad837-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ad837-130">System.String</span></span>

## <span data-ttu-id="ad837-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad837-131">OUTPUTS</span></span>

### <span data-ttu-id="ad837-132">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="ad837-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="ad837-133">Note</span><span class="sxs-lookup"><span data-stu-id="ad837-133">NOTES</span></span>
<span data-ttu-id="ad837-134">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="ad837-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ad837-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad837-135">RELATED LINKS</span></span>
