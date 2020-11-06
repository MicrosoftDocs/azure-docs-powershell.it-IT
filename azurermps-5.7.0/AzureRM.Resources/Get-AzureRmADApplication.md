---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: b44d3bbf7c594f5f9114488b536d28fd17fe56c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519877"
---
# <span data-ttu-id="ab938-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ab938-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="ab938-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab938-102">SYNOPSIS</span></span>
<span data-ttu-id="ab938-103">Elenca le applicazioni di Azure Active Directory esistenti.</span><span class="sxs-lookup"><span data-stu-id="ab938-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab938-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab938-104">SYNTAX</span></span>

### <span data-ttu-id="ab938-105">EmptyParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ab938-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab938-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab938-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab938-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab938-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab938-108">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab938-108">ApplicationDisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab938-109">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab938-109">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab938-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab938-110">DESCRIPTION</span></span>
<span data-ttu-id="ab938-111">Elenca le applicazioni di Azure Active Directory esistenti.</span><span class="sxs-lookup"><span data-stu-id="ab938-111">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="ab938-112">La ricerca dell'applicazione può essere eseguita da ObjectId, ApplicationId, IdentifierUri o DisplayName.</span><span class="sxs-lookup"><span data-stu-id="ab938-112">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="ab938-113">Se non viene specificato alcun parametro, recupera tutte le applicazioni sotto il tenant.</span><span class="sxs-lookup"><span data-stu-id="ab938-113">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="ab938-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab938-114">EXAMPLES</span></span>

### <span data-ttu-id="ab938-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ab938-115">Example 1</span></span>
```
PS E:\> Get-AzureRmADApplication
```

<span data-ttu-id="ab938-116">Elenca tutte le applicazioni in un tenant.</span><span class="sxs-lookup"><span data-stu-id="ab938-116">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="ab938-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ab938-117">Example 2</span></span>
```
PS E:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="ab938-118">Ottiene l'applicazione con URI dell'identificatore come " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="ab938-118">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

## <span data-ttu-id="ab938-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab938-119">PARAMETERS</span></span>

### <span data-ttu-id="ab938-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ab938-120">-ApplicationId</span></span>
<span data-ttu-id="ab938-121">ID applicazione dell'applicazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="ab938-121">The application id of the application to fetch.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab938-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab938-122">-DefaultProfile</span></span>
<span data-ttu-id="ab938-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ab938-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab938-124">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="ab938-124">-DisplayNameStartWith</span></span>
<span data-ttu-id="ab938-125">Recuperare tutte le applicazioni che iniziano con il nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="ab938-125">Fetch all applications starting with the display name.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab938-126">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="ab938-126">-IdentifierUri</span></span>
<span data-ttu-id="ab938-127">URI identificatore univoco dell'applicazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="ab938-127">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab938-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ab938-128">-ObjectId</span></span>
<span data-ttu-id="ab938-129">ID oggetto dell'applicazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="ab938-129">The object id of the application to fetch.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab938-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab938-130">CommonParameters</span></span>
<span data-ttu-id="ab938-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab938-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab938-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab938-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab938-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab938-133">INPUTS</span></span>

### <span data-ttu-id="ab938-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ab938-134">None</span></span>
<span data-ttu-id="ab938-135">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="ab938-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ab938-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab938-136">OUTPUTS</span></span>

### <span data-ttu-id="ab938-137">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication]</span><span class="sxs-lookup"><span data-stu-id="ab938-137">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication]</span></span>

## <span data-ttu-id="ab938-138">Note</span><span class="sxs-lookup"><span data-stu-id="ab938-138">NOTES</span></span>

## <span data-ttu-id="ab938-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab938-139">RELATED LINKS</span></span>

[<span data-ttu-id="ab938-140">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ab938-140">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="ab938-141">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ab938-141">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="ab938-142">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ab938-142">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="ab938-143">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ab938-143">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="ab938-144">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ab938-144">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="ab938-145">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ab938-145">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

