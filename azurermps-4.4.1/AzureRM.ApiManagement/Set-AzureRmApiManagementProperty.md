---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
ms.openlocfilehash: 5273161b18f49e2cfd8f772987d8f0d9ce90bc69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508783"
---
# <span data-ttu-id="eb086-101">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="eb086-101">Set-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="eb086-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eb086-102">SYNOPSIS</span></span>
<span data-ttu-id="eb086-103">Modifica una proprietà di gestione API.</span><span class="sxs-lookup"><span data-stu-id="eb086-103">Modifies an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb086-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb086-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tags <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb086-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb086-105">DESCRIPTION</span></span>
<span data-ttu-id="eb086-106">Il cmdlet **set-AzureRmApiManagementProperty** modifica una proprietà di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="eb086-106">The **Set-AzureRmApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="eb086-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb086-107">EXAMPLES</span></span>

### <span data-ttu-id="eb086-108">Esempio 1: modificare i tag in una proprietà</span><span class="sxs-lookup"><span data-stu-id="eb086-108">Example 1: Change the tags on a property</span></span>
```
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="eb086-109">Il primo comando assegna due valori alla variabile $Tags.</span><span class="sxs-lookup"><span data-stu-id="eb086-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="eb086-110">Il secondo comando modifica la proprietà che contiene l'ID Property11.</span><span class="sxs-lookup"><span data-stu-id="eb086-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="eb086-111">Il comando assegna le stringhe in $Tags come tag nella proprietà.</span><span class="sxs-lookup"><span data-stu-id="eb086-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="eb086-112">Esempio 2: modificare una proprietà per avere un valore segreto</span><span class="sxs-lookup"><span data-stu-id="eb086-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>Set-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="eb086-113">Questo comando modifica la proprietà da crittografare.</span><span class="sxs-lookup"><span data-stu-id="eb086-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="eb086-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eb086-114">PARAMETERS</span></span>

### <span data-ttu-id="eb086-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="eb086-115">-Context</span></span>
<span data-ttu-id="eb086-116">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="eb086-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="eb086-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb086-117">-Name</span></span>
<span data-ttu-id="eb086-118">Specifica il nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="eb086-118">Specifies the name of the property.</span></span>
<span data-ttu-id="eb086-119">La lunghezza massima è di 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="eb086-119">Maximum length is 100 characters.</span></span>
<span data-ttu-id="eb086-120">I nomi contengono solo lettere, cifre, punto, trattino e caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="eb086-120">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="eb086-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb086-121">-PassThru</span></span>
<span data-ttu-id="eb086-122">Indica che questo cmdlet restituisce il **PsApiManagementProperty** modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb086-122">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="eb086-123">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="eb086-123">-PropertyId</span></span>
<span data-ttu-id="eb086-124">Specifica un ID della proprietà modificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb086-124">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="eb086-125">-Segreto</span><span class="sxs-lookup"><span data-stu-id="eb086-125">-Secret</span></span>
<span data-ttu-id="eb086-126">Indica che il valore della proprietà è un segreto e deve essere crittografato.</span><span class="sxs-lookup"><span data-stu-id="eb086-126">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb086-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="eb086-127">-Tags</span></span>
<span data-ttu-id="eb086-128">Specifica una matrice di tag che questo cmdlet associa alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="eb086-128">Specifies an array of tags that this cmdlet associates to the property.</span></span>
<span data-ttu-id="eb086-129">Puoi usare i tag per filtrare l'elenco delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="eb086-129">You can use tags to filter the property list.</span></span>

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

### <span data-ttu-id="eb086-130">-Valore</span><span class="sxs-lookup"><span data-stu-id="eb086-130">-Value</span></span>
<span data-ttu-id="eb086-131">Specifica un valore per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="eb086-131">Specifies a value for the property.</span></span>
<span data-ttu-id="eb086-132">Questo valore può contenere espressioni di criteri.</span><span class="sxs-lookup"><span data-stu-id="eb086-132">This value can contain policy expressions.</span></span>
<span data-ttu-id="eb086-133">La lunghezza massima è di 1000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="eb086-133">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="eb086-134">Il valore potrebbe non essere vuoto o costituito solo da spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="eb086-134">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="eb086-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb086-135">-DefaultProfile</span></span>
<span data-ttu-id="eb086-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eb086-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb086-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb086-137">CommonParameters</span></span>
<span data-ttu-id="eb086-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb086-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb086-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb086-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb086-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eb086-140">INPUTS</span></span>

## <span data-ttu-id="eb086-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb086-141">OUTPUTS</span></span>

### <span data-ttu-id="eb086-142">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="eb086-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="eb086-143">Note</span><span class="sxs-lookup"><span data-stu-id="eb086-143">NOTES</span></span>

## <span data-ttu-id="eb086-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb086-144">RELATED LINKS</span></span>

[<span data-ttu-id="eb086-145">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="eb086-145">Get-AzureRmApiManagementProperty</span></span>](./Get-AzureRmApiManagementProperty.md)

[<span data-ttu-id="eb086-146">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="eb086-146">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="eb086-147">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="eb086-147">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)


