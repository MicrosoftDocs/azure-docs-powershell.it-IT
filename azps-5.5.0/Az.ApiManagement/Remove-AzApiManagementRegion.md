---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 70816b054acc7667d2246ea72901c65890f9389e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210315"
---
# <span data-ttu-id="04dc8-101">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="04dc8-101">Remove-AzApiManagementRegion</span></span>

## <span data-ttu-id="04dc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="04dc8-103">Rimuove un'area di distribuzione esistente dall'istanza di PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="04dc8-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

## <span data-ttu-id="04dc8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04dc8-104">SYNTAX</span></span>

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04dc8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="04dc8-105">DESCRIPTION</span></span>
<span data-ttu-id="04dc8-106">Il cmdlet **Remove-AzApiManagementRegion** rimuove un'istanza del tipo **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** da una raccolta **di AdditionalRegions** di provided l'istanza di **tipo Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="04dc8-106">The **Remove-AzApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="04dc8-107">Questo cmdlet non modifica la distribuzione da sola ma aggiorna l'istanza di **PsApiManagement** in memoria.</span><span class="sxs-lookup"><span data-stu-id="04dc8-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="04dc8-108">Per aggiornare una distribuzione di Gestione API, passare **psApiManagementInstance modificata** a **Set-AzApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="04dc8-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Set-AzApiManagement**.</span></span>

## <span data-ttu-id="04dc8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04dc8-109">EXAMPLES</span></span>

### <span data-ttu-id="04dc8-110">Esempio 1: Rimuovere un'area da un'istanza di PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="04dc8-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="04dc8-111">Questo comando rimuove l'area geografica denominata Stati Uniti orientali **dall'istanza PsApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="04dc8-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="04dc8-112">Esempio 2: Rimuovere un'area da un'istanza di PsApiManagement usando una serie di comandi</span><span class="sxs-lookup"><span data-stu-id="04dc8-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

<span data-ttu-id="04dc8-113">Il primo comando ottiene un'istanza di **PsApiManagement** dal gruppo di risorse contoso denominato ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="04dc8-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="04dc8-114">Il comando finale rimuove quindi l'area geografica denominata Stati Uniti orientali da tale istanza e quindi aggiorna la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="04dc8-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="04dc8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04dc8-115">PARAMETERS</span></span>

### <span data-ttu-id="04dc8-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="04dc8-116">-ApiManagement</span></span>
<span data-ttu-id="04dc8-117">Specifica **l'istanza PsApiManagement** da cui questo cmdlet rimuove l'area di distribuzione aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="04dc8-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04dc8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04dc8-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="04dc8-119">-Location</span><span class="sxs-lookup"><span data-stu-id="04dc8-119">-Location</span></span>
<span data-ttu-id="04dc8-120">Specifica la posizione dell'area geografica rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04dc8-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="04dc8-121">Specifica la posizione della nuova area di distribuzione tra l'area supportata per il servizio di gestione api.</span><span class="sxs-lookup"><span data-stu-id="04dc8-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="04dc8-122">Per ottenere posizioni valide, usare il cmdlet Get-AzResourceProvider -ProviderManagement "Microsoft.ApiManagement" | dove {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object percorsi</span><span class="sxs-lookup"><span data-stu-id="04dc8-122">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="04dc8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04dc8-123">CommonParameters</span></span>
<span data-ttu-id="04dc8-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04dc8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04dc8-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="04dc8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04dc8-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="04dc8-126">INPUTS</span></span>

### <span data-ttu-id="04dc8-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="04dc8-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="04dc8-128">System.String</span><span class="sxs-lookup"><span data-stu-id="04dc8-128">System.String</span></span>

## <span data-ttu-id="04dc8-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04dc8-129">OUTPUTS</span></span>

### <span data-ttu-id="04dc8-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="04dc8-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="04dc8-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="04dc8-131">NOTES</span></span>

## <span data-ttu-id="04dc8-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04dc8-132">RELATED LINKS</span></span>

[<span data-ttu-id="04dc8-133">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="04dc8-133">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="04dc8-134">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="04dc8-134">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)


