---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: c5276ddbcd10870355f8530c2f04f81122dda382
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686157"
---
# <span data-ttu-id="2fcbd-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="2fcbd-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="2fcbd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2fcbd-102">SYNOPSIS</span></span>
<span data-ttu-id="2fcbd-103">Elenca le applicazioni di Azure Active Directory esistenti.</span><span class="sxs-lookup"><span data-stu-id="2fcbd-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fcbd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fcbd-104">SYNTAX</span></span>

### <span data-ttu-id="2fcbd-105">EmptyParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2fcbd-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fcbd-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fcbd-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fcbd-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fcbd-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fcbd-108">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fcbd-108">ApplicationDisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fcbd-109">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fcbd-109">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2fcbd-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fcbd-110">DESCRIPTION</span></span>
<span data-ttu-id="2fcbd-111">Elenca le applicazioni di Azure Active Directory esistenti.</span><span class="sxs-lookup"><span data-stu-id="2fcbd-111">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="2fcbd-112">La ricerca dell'applicazione può essere eseguita da ObjectId, ApplicationId, IdentifierUri o DisplayName.</span><span class="sxs-lookup"><span data-stu-id="2fcbd-112">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="2fcbd-113">Se non viene specificato alcun parametro, recupera tutte le applicazioni sotto il tenant.</span><span class="sxs-lookup"><span data-stu-id="2fcbd-113">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="2fcbd-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fcbd-114">EXAMPLES</span></span>

### <span data-ttu-id="2fcbd-115">--------------------------Esempio 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2fcbd-115">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADApplication
```

<span data-ttu-id="2fcbd-116">Elenca tutte le applicazioni in un tenant.</span><span class="sxs-lookup"><span data-stu-id="2fcbd-116">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="2fcbd-117">--------------------------Esempio 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="2fcbd-117">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="2fcbd-118">Ottiene l'applicazione con URI dell'identificatore come " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="2fcbd-118">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

## <span data-ttu-id="2fcbd-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2fcbd-119">PARAMETERS</span></span>

### <span data-ttu-id="2fcbd-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2fcbd-120">-ApplicationId</span></span>
<span data-ttu-id="2fcbd-121">ID applicazione dell'applicazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="2fcbd-121">The application id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fcbd-122">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="2fcbd-122">-DisplayNameStartWith</span></span>
<span data-ttu-id="2fcbd-123">Recuperare tutte le applicazioni che iniziano con il nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="2fcbd-123">Fetch all applications starting with the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fcbd-124">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="2fcbd-124">-IdentifierUri</span></span>
<span data-ttu-id="2fcbd-125">URI identificatore univoco dell'applicazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="2fcbd-125">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fcbd-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2fcbd-126">-ObjectId</span></span>
<span data-ttu-id="2fcbd-127">ID oggetto dell'applicazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="2fcbd-127">The object id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fcbd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fcbd-128">-DefaultProfile</span></span>
<span data-ttu-id="2fcbd-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2fcbd-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fcbd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fcbd-130">CommonParameters</span></span>
<span data-ttu-id="2fcbd-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fcbd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fcbd-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fcbd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fcbd-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2fcbd-133">INPUTS</span></span>

## <span data-ttu-id="2fcbd-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fcbd-134">OUTPUTS</span></span>

### <span data-ttu-id="2fcbd-135">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication]</span><span class="sxs-lookup"><span data-stu-id="2fcbd-135">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication]</span></span>

## <span data-ttu-id="2fcbd-136">Note</span><span class="sxs-lookup"><span data-stu-id="2fcbd-136">NOTES</span></span>

## <span data-ttu-id="2fcbd-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fcbd-137">RELATED LINKS</span></span>

[<span data-ttu-id="2fcbd-138">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="2fcbd-138">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="2fcbd-139">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="2fcbd-139">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="2fcbd-140">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="2fcbd-140">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="2fcbd-141">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="2fcbd-141">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="2fcbd-142">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="2fcbd-142">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="2fcbd-143">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="2fcbd-143">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

