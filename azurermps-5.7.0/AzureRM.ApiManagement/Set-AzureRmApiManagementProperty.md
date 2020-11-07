---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
ms.openlocfilehash: 89612136023173d2f725c8c4b286a270400f8c6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687655"
---
# <span data-ttu-id="84312-101">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="84312-101">Set-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="84312-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84312-102">SYNOPSIS</span></span>
<span data-ttu-id="84312-103">Modifica una proprietà di gestione API.</span><span class="sxs-lookup"><span data-stu-id="84312-103">Modifies an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84312-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84312-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84312-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84312-105">DESCRIPTION</span></span>
<span data-ttu-id="84312-106">Il cmdlet **set-AzureRmApiManagementProperty** modifica una proprietà di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="84312-106">The **Set-AzureRmApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="84312-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84312-107">EXAMPLES</span></span>

### <span data-ttu-id="84312-108">Esempio 1: modificare i tag in una proprietà</span><span class="sxs-lookup"><span data-stu-id="84312-108">Example 1: Change the tags on a property</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="84312-109">Il primo comando assegna due valori alla variabile $Tags.</span><span class="sxs-lookup"><span data-stu-id="84312-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="84312-110">Il secondo comando modifica la proprietà che contiene l'ID Property11.</span><span class="sxs-lookup"><span data-stu-id="84312-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="84312-111">Il comando assegna le stringhe in $Tags come tag nella proprietà.</span><span class="sxs-lookup"><span data-stu-id="84312-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="84312-112">Esempio 2: modificare una proprietà per avere un valore segreto</span><span class="sxs-lookup"><span data-stu-id="84312-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="84312-113">Questo comando modifica la proprietà da crittografare.</span><span class="sxs-lookup"><span data-stu-id="84312-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="84312-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84312-114">PARAMETERS</span></span>

### <span data-ttu-id="84312-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="84312-115">-Context</span></span>
<span data-ttu-id="84312-116">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="84312-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84312-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84312-117">-DefaultProfile</span></span>
<span data-ttu-id="84312-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84312-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84312-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="84312-119">-Name</span></span>
<span data-ttu-id="84312-120">Specifica il nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="84312-120">Specifies the name of the property.</span></span>
<span data-ttu-id="84312-121">La lunghezza massima è di 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="84312-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="84312-122">I nomi contengono solo lettere, cifre, punto, trattino e caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="84312-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="84312-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84312-123">-PassThru</span></span>
<span data-ttu-id="84312-124">Indica che questo cmdlet restituisce il **PsApiManagementProperty** modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84312-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84312-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="84312-125">-PropertyId</span></span>
<span data-ttu-id="84312-126">Specifica un ID della proprietà modificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84312-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="84312-127">-Segreto</span><span class="sxs-lookup"><span data-stu-id="84312-127">-Secret</span></span>
<span data-ttu-id="84312-128">Indica che il valore della proprietà è un segreto e deve essere crittografato.</span><span class="sxs-lookup"><span data-stu-id="84312-128">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84312-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="84312-129">-Tag</span></span>
<span data-ttu-id="84312-130">Tag associati a una proprietà.</span><span class="sxs-lookup"><span data-stu-id="84312-130">Tags associated with a property.</span></span> <span data-ttu-id="84312-131">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="84312-131">This parameter is optional.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84312-132">-Valore</span><span class="sxs-lookup"><span data-stu-id="84312-132">-Value</span></span>
<span data-ttu-id="84312-133">Specifica un valore per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="84312-133">Specifies a value for the property.</span></span>
<span data-ttu-id="84312-134">Questo valore può contenere espressioni di criteri.</span><span class="sxs-lookup"><span data-stu-id="84312-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="84312-135">La lunghezza massima è di 1000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="84312-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="84312-136">Il valore potrebbe non essere vuoto o costituito solo da spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="84312-136">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="84312-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84312-137">CommonParameters</span></span>
<span data-ttu-id="84312-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84312-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84312-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84312-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84312-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84312-140">INPUTS</span></span>

### <span data-ttu-id="84312-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="84312-141">None</span></span>
<span data-ttu-id="84312-142">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="84312-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="84312-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84312-143">OUTPUTS</span></span>

### <span data-ttu-id="84312-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="84312-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="84312-145">Note</span><span class="sxs-lookup"><span data-stu-id="84312-145">NOTES</span></span>

## <span data-ttu-id="84312-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84312-146">RELATED LINKS</span></span>

[<span data-ttu-id="84312-147">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="84312-147">Get-AzureRmApiManagementProperty</span></span>](./Get-AzureRmApiManagementProperty.md)

[<span data-ttu-id="84312-148">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="84312-148">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="84312-149">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="84312-149">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)

