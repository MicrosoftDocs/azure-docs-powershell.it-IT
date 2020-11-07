---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
ms.openlocfilehash: 4e7abd4a3b33f54e5a0ec0bdde01e3fe11da31c4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866211"
---
# <span data-ttu-id="fb3f4-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="fb3f4-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="fb3f4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb3f4-102">SYNOPSIS</span></span>
<span data-ttu-id="fb3f4-103">Elenca le applicazioni di Azure Active Directory esistenti.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb3f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb3f4-104">SYNTAX</span></span>

### <span data-ttu-id="fb3f4-105">EmptyParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fb3f4-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="fb3f4-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb3f4-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="fb3f4-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb3f4-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="fb3f4-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb3f4-108">SearchStringParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="fb3f4-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb3f4-109">DisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="fb3f4-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb3f4-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="fb3f4-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb3f4-111">DESCRIPTION</span></span>
<span data-ttu-id="fb3f4-112">Elenca le applicazioni di Azure Active Directory esistenti.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="fb3f4-113">La ricerca dell'applicazione può essere eseguita da ObjectId, ApplicationId, IdentifierUri o DisplayName.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="fb3f4-114">Se non viene specificato alcun parametro, recupera tutte le applicazioni sotto il tenant.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="fb3f4-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb3f4-115">EXAMPLES</span></span>

### <span data-ttu-id="fb3f4-116">Esempio 1-elenca tutte le applicazioni</span><span class="sxs-lookup"><span data-stu-id="fb3f4-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzureRmADApplication
```

<span data-ttu-id="fb3f4-117">Elenca tutte le applicazioni in un tenant.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="fb3f4-118">Esempio 2-elenco delle applicazioni che usano il paging</span><span class="sxs-lookup"><span data-stu-id="fb3f4-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzureRmADApplication -First 100
```

<span data-ttu-id="fb3f4-119">Elenca le prime applicazioni di 100 in un tenant.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="fb3f4-120">Esempio 3-ottenere l'applicazione dall'URI dell'identificatore</span><span class="sxs-lookup"><span data-stu-id="fb3f4-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="fb3f4-121">Ottiene l'applicazione con URI dell'identificatore come " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="fb3f4-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="fb3f4-122">Esempio 4-ottenere l'applicazione dall'ID oggetto</span><span class="sxs-lookup"><span data-stu-id="fb3f4-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="fb3f4-123">Ottiene l'applicazione con l'ID oggetto "39e64ec6-569B-4030-8e1c-c3c519a05d69".</span><span class="sxs-lookup"><span data-stu-id="fb3f4-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="fb3f4-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb3f4-124">PARAMETERS</span></span>

### <span data-ttu-id="fb3f4-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="fb3f4-125">-ApplicationId</span></span>
<span data-ttu-id="fb3f4-126">ID applicazione dell'applicazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="fb3f4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb3f4-127">-DefaultProfile</span></span>
<span data-ttu-id="fb3f4-128">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fb3f4-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb3f4-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fb3f4-129">-DisplayName</span></span>
<span data-ttu-id="fb3f4-130">Nome visualizzato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-130">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb3f4-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="fb3f4-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="fb3f4-132">Recuperare tutte le applicazioni che iniziano con il nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-132">Fetch all applications starting with the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb3f4-133">-Primo</span><span class="sxs-lookup"><span data-stu-id="fb3f4-133">-First</span></span>
<span data-ttu-id="fb3f4-134">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-134">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3f4-135">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="fb3f4-135">-IdentifierUri</span></span>
<span data-ttu-id="fb3f4-136">URI identificatore univoco dell'applicazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-136">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="fb3f4-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="fb3f4-137">-IncludeTotalCount</span></span>
<span data-ttu-id="fb3f4-138">Segnala il numero di oggetti nel set di dati.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="fb3f4-139">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="fb3f4-140">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fb3f4-140">-ObjectId</span></span>
<span data-ttu-id="fb3f4-141">ID oggetto dell'applicazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-141">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="fb3f4-142">-Skip</span><span class="sxs-lookup"><span data-stu-id="fb3f4-142">-Skip</span></span>
<span data-ttu-id="fb3f4-143">Ignora i primi oggetti N e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-143">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3f4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb3f4-144">CommonParameters</span></span>
<span data-ttu-id="fb3f4-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb3f4-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb3f4-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb3f4-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb3f4-147">INPUTS</span></span>

### <span data-ttu-id="fb3f4-148">System. Guid</span><span class="sxs-lookup"><span data-stu-id="fb3f4-148">System.Guid</span></span>

### <span data-ttu-id="fb3f4-149">System. String</span><span class="sxs-lookup"><span data-stu-id="fb3f4-149">System.String</span></span>

## <span data-ttu-id="fb3f4-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb3f4-150">OUTPUTS</span></span>

### <span data-ttu-id="fb3f4-151">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="fb3f4-151">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="fb3f4-152">Note</span><span class="sxs-lookup"><span data-stu-id="fb3f4-152">NOTES</span></span>

## <span data-ttu-id="fb3f4-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb3f4-153">RELATED LINKS</span></span>

[<span data-ttu-id="fb3f4-154">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="fb3f4-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="fb3f4-155">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="fb3f4-155">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="fb3f4-156">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="fb3f4-156">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="fb3f4-157">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="fb3f4-157">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)



[<span data-ttu-id="fb3f4-158">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="fb3f4-158">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

