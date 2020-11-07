---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
ms.openlocfilehash: d54665b767d10edde564450ecfcdd467b784dd8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852534"
---
# <span data-ttu-id="94f6b-101">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="94f6b-101">New-AzApiManagementProperty</span></span>

## <span data-ttu-id="94f6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="94f6b-102">SYNOPSIS</span></span>
<span data-ttu-id="94f6b-103">Crea una nuova proprietà.</span><span class="sxs-lookup"><span data-stu-id="94f6b-103">Creates a new Property.</span></span>

## <span data-ttu-id="94f6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94f6b-104">SYNTAX</span></span>

```
New-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94f6b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94f6b-105">DESCRIPTION</span></span>
<span data-ttu-id="94f6b-106">Il cmdlet **New-AzApiManagementProperty** crea una **Proprietà** di gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="94f6b-106">The **New-AzApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="94f6b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94f6b-107">EXAMPLES</span></span>

### <span data-ttu-id="94f6b-108">Esempio 1: creare una proprietà che include tag</span><span class="sxs-lookup"><span data-stu-id="94f6b-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="94f6b-109">Il primo comando assegna due valori alla variabile $Tags.</span><span class="sxs-lookup"><span data-stu-id="94f6b-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="94f6b-110">Il secondo comando crea una proprietà e assegna le stringhe in $Tags come tag nella proprietà.</span><span class="sxs-lookup"><span data-stu-id="94f6b-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="94f6b-111">Esempio 2: creare una proprietà con un valore segreto</span><span class="sxs-lookup"><span data-stu-id="94f6b-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="94f6b-112">Questo comando crea una **Proprietà** con un valore crittografato.</span><span class="sxs-lookup"><span data-stu-id="94f6b-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="94f6b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="94f6b-113">PARAMETERS</span></span>

### <span data-ttu-id="94f6b-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="94f6b-114">-Context</span></span>
<span data-ttu-id="94f6b-115">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="94f6b-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f6b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f6b-116">-DefaultProfile</span></span>
<span data-ttu-id="94f6b-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94f6b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94f6b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="94f6b-118">-Name</span></span>
<span data-ttu-id="94f6b-119">Specifica il nome della proprietà creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94f6b-119">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="94f6b-120">La lunghezza massima è di 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="94f6b-120">Maximum length is 100 characters.</span></span>
<span data-ttu-id="94f6b-121">I nomi contengono solo lettere, cifre, punto, trattino e caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="94f6b-121">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="94f6b-122">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="94f6b-122">-PropertyId</span></span>
<span data-ttu-id="94f6b-123">Specifica un ID per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="94f6b-123">Specifies an ID for the property.</span></span>
<span data-ttu-id="94f6b-124">La lunghezza massima è di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="94f6b-124">Maximum length is 256 characters.</span></span>
<span data-ttu-id="94f6b-125">Se non specifichi un ID, questo cmdlet ne genera uno.</span><span class="sxs-lookup"><span data-stu-id="94f6b-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="94f6b-126">-Segreto</span><span class="sxs-lookup"><span data-stu-id="94f6b-126">-Secret</span></span>
<span data-ttu-id="94f6b-127">Indica che il valore della proprietà è un segreto e deve essere crittografato.</span><span class="sxs-lookup"><span data-stu-id="94f6b-127">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="94f6b-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="94f6b-128">-Tag</span></span>
<span data-ttu-id="94f6b-129">Tag da associare alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="94f6b-129">Tags to be associated with Property.</span></span> <span data-ttu-id="94f6b-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="94f6b-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="94f6b-131">-Valore</span><span class="sxs-lookup"><span data-stu-id="94f6b-131">-Value</span></span>
<span data-ttu-id="94f6b-132">Specifica un valore per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="94f6b-132">Specifies a value for the property.</span></span>
<span data-ttu-id="94f6b-133">Questo valore può contenere espressioni di criteri.</span><span class="sxs-lookup"><span data-stu-id="94f6b-133">This value can contain policy expressions.</span></span>
<span data-ttu-id="94f6b-134">La lunghezza massima è di 1000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="94f6b-134">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="94f6b-135">Il valore potrebbe non essere vuoto o costituito solo da spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="94f6b-135">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="94f6b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f6b-136">CommonParameters</span></span>
<span data-ttu-id="94f6b-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94f6b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f6b-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94f6b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f6b-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="94f6b-139">INPUTS</span></span>

### <span data-ttu-id="94f6b-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="94f6b-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="94f6b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="94f6b-141">System.String</span></span>

### <span data-ttu-id="94f6b-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="94f6b-142">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="94f6b-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="94f6b-143">System.String[]</span></span>

## <span data-ttu-id="94f6b-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94f6b-144">OUTPUTS</span></span>

### <span data-ttu-id="94f6b-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="94f6b-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="94f6b-146">Note</span><span class="sxs-lookup"><span data-stu-id="94f6b-146">NOTES</span></span>

## <span data-ttu-id="94f6b-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94f6b-147">RELATED LINKS</span></span>

[<span data-ttu-id="94f6b-148">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="94f6b-148">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)

[<span data-ttu-id="94f6b-149">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="94f6b-149">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)


