---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: aacc24926bf38f52f1fd273847e48082c8d110c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981214"
---
# <span data-ttu-id="d02e0-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="d02e0-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="d02e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d02e0-102">SYNOPSIS</span></span>
<span data-ttu-id="d02e0-103">Recupera i tipi di account di Servizi cognitivi disponibili.</span><span class="sxs-lookup"><span data-stu-id="d02e0-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="d02e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d02e0-104">SYNTAX</span></span>

### <span data-ttu-id="d02e0-105">GetAccountTypes (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d02e0-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d02e0-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="d02e0-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d02e0-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d02e0-107">DESCRIPTION</span></span>
<span data-ttu-id="d02e0-108">Il cmdlet **Get-AzCognitiveServicesAccountType** ottiene i tipi di account di Servizi cognitivi disponibili in questa sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="d02e0-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="d02e0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d02e0-109">EXAMPLES</span></span>

### <span data-ttu-id="d02e0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d02e0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="d02e0-111">Ottenere l'elenco dei tipi disponibili.</span><span class="sxs-lookup"><span data-stu-id="d02e0-111">Get the list of available Types.</span></span>

### <span data-ttu-id="d02e0-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d02e0-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="d02e0-113">Ottenere l'elenco dei tipi disponibili in Westus.</span><span class="sxs-lookup"><span data-stu-id="d02e0-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="d02e0-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d02e0-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="d02e0-115">Verificare se si tratta di un nome Tipo valido, verrà restituito il nome `Face` se si tratta di un nome valido.</span><span class="sxs-lookup"><span data-stu-id="d02e0-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="d02e0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d02e0-116">PARAMETERS</span></span>

### <span data-ttu-id="d02e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d02e0-117">-DefaultProfile</span></span>
<span data-ttu-id="d02e0-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d02e0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d02e0-119">-Location</span><span class="sxs-lookup"><span data-stu-id="d02e0-119">-Location</span></span>
<span data-ttu-id="d02e0-120">Posizione dell'account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="d02e0-120">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypes
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d02e0-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="d02e0-121">-TypeName</span></span>
<span data-ttu-id="d02e0-122">Nome del tipo di account dei Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="d02e0-122">Cognitive Services Account Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypeWithName
Aliases: CognitiveServicesAccountTypeName, AccountTypeName, KindName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d02e0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d02e0-123">CommonParameters</span></span>
<span data-ttu-id="d02e0-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d02e0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d02e0-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d02e0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d02e0-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="d02e0-126">INPUTS</span></span>

### <span data-ttu-id="d02e0-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d02e0-127">System.String</span></span>

## <span data-ttu-id="d02e0-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d02e0-128">OUTPUTS</span></span>

### <span data-ttu-id="d02e0-129">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d02e0-129">System.String[]</span></span>

### <span data-ttu-id="d02e0-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d02e0-130">System.String</span></span>

## <span data-ttu-id="d02e0-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="d02e0-131">NOTES</span></span>

## <span data-ttu-id="d02e0-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d02e0-132">RELATED LINKS</span></span>
