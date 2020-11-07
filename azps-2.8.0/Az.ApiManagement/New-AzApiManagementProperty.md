---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
ms.openlocfilehash: 816e1ee8af966e7c0a3c296d3e971d69134c103e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675989"
---
# <span data-ttu-id="7b121-101">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="7b121-101">New-AzApiManagementProperty</span></span>

## <span data-ttu-id="7b121-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b121-102">SYNOPSIS</span></span>
<span data-ttu-id="7b121-103">Crea una nuova proprietà.</span><span class="sxs-lookup"><span data-stu-id="7b121-103">Creates a new Property.</span></span>

## <span data-ttu-id="7b121-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b121-104">SYNTAX</span></span>

```
New-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b121-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b121-105">DESCRIPTION</span></span>
<span data-ttu-id="7b121-106">Il cmdlet **New-AzApiManagementProperty** crea una **Proprietà** di gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b121-106">The **New-AzApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="7b121-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b121-107">EXAMPLES</span></span>

### <span data-ttu-id="7b121-108">Esempio 1: creare una proprietà che include tag</span><span class="sxs-lookup"><span data-stu-id="7b121-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="7b121-109">Il primo comando assegna due valori alla variabile $Tags.</span><span class="sxs-lookup"><span data-stu-id="7b121-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="7b121-110">Il secondo comando crea una proprietà e assegna le stringhe in $Tags come tag nella proprietà.</span><span class="sxs-lookup"><span data-stu-id="7b121-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="7b121-111">Esempio 2: creare una proprietà con un valore segreto</span><span class="sxs-lookup"><span data-stu-id="7b121-111">Example 2: Create a property that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="7b121-112">Questo comando crea una **Proprietà** con un valore crittografato.</span><span class="sxs-lookup"><span data-stu-id="7b121-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="7b121-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b121-113">PARAMETERS</span></span>

### <span data-ttu-id="7b121-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="7b121-114">-Context</span></span>
<span data-ttu-id="7b121-115">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7b121-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b121-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b121-116">-DefaultProfile</span></span>
<span data-ttu-id="7b121-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b121-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b121-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b121-118">-Name</span></span>
<span data-ttu-id="7b121-119">Specifica il nome della proprietà creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b121-119">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="7b121-120">La lunghezza massima è di 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="7b121-120">Maximum length is 100 characters.</span></span>
<span data-ttu-id="7b121-121">I nomi contengono solo lettere, cifre, punto, trattino e caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="7b121-121">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="7b121-122">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="7b121-122">-PropertyId</span></span>
<span data-ttu-id="7b121-123">Specifica un ID per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="7b121-123">Specifies an ID for the property.</span></span>
<span data-ttu-id="7b121-124">La lunghezza massima è di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="7b121-124">Maximum length is 256 characters.</span></span>
<span data-ttu-id="7b121-125">Se non specifichi un ID, questo cmdlet ne genera uno.</span><span class="sxs-lookup"><span data-stu-id="7b121-125">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b121-126">-Segreto</span><span class="sxs-lookup"><span data-stu-id="7b121-126">-Secret</span></span>
<span data-ttu-id="7b121-127">Indica che il valore della proprietà è un segreto e deve essere crittografato.</span><span class="sxs-lookup"><span data-stu-id="7b121-127">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b121-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="7b121-128">-Tag</span></span>
<span data-ttu-id="7b121-129">Tag da associare alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="7b121-129">Tags to be associated with Property.</span></span> <span data-ttu-id="7b121-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="7b121-130">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b121-131">-Valore</span><span class="sxs-lookup"><span data-stu-id="7b121-131">-Value</span></span>
<span data-ttu-id="7b121-132">Specifica un valore per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="7b121-132">Specifies a value for the property.</span></span>
<span data-ttu-id="7b121-133">Questo valore può contenere espressioni di criteri.</span><span class="sxs-lookup"><span data-stu-id="7b121-133">This value can contain policy expressions.</span></span>
<span data-ttu-id="7b121-134">La lunghezza massima è di 1000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="7b121-134">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="7b121-135">Il valore potrebbe non essere vuoto o costituito solo da spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="7b121-135">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="7b121-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b121-136">CommonParameters</span></span>
<span data-ttu-id="7b121-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b121-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b121-138">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b121-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b121-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b121-139">INPUTS</span></span>

### <span data-ttu-id="7b121-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7b121-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7b121-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7b121-141">System.String</span></span>

### <span data-ttu-id="7b121-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7b121-142">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7b121-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="7b121-143">System.String[]</span></span>

## <span data-ttu-id="7b121-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b121-144">OUTPUTS</span></span>

### <span data-ttu-id="7b121-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="7b121-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="7b121-146">Note</span><span class="sxs-lookup"><span data-stu-id="7b121-146">NOTES</span></span>

## <span data-ttu-id="7b121-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b121-147">RELATED LINKS</span></span>

[<span data-ttu-id="7b121-148">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="7b121-148">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)

[<span data-ttu-id="7b121-149">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="7b121-149">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)

