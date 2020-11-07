---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
ms.openlocfilehash: 78523d5bef3bfb2461bb524044da14f8aedbbc12
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866453"
---
# <span data-ttu-id="e42bd-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="e42bd-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="e42bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e42bd-102">SYNOPSIS</span></span>
<span data-ttu-id="e42bd-103">Filtra gli utenti di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e42bd-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e42bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e42bd-104">SYNTAX</span></span>

### <span data-ttu-id="e42bd-105">EmptyParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e42bd-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e42bd-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="e42bd-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e42bd-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e42bd-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e42bd-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e42bd-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e42bd-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e42bd-109">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e42bd-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="e42bd-110">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="e42bd-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e42bd-111">DESCRIPTION</span></span>
<span data-ttu-id="e42bd-112">Filtra gli utenti di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e42bd-112">Filters active directory users.</span></span>

## <span data-ttu-id="e42bd-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e42bd-113">EXAMPLES</span></span>

### <span data-ttu-id="e42bd-114">Esempio 1-elenca tutti gli utenti</span><span class="sxs-lookup"><span data-stu-id="e42bd-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="e42bd-115">Elenca tutti gli utenti degli annunci in un tenant.</span><span class="sxs-lookup"><span data-stu-id="e42bd-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="e42bd-116">Esempio 2-elenca tutti gli utenti che usano il paging</span><span class="sxs-lookup"><span data-stu-id="e42bd-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzureRmADUser -First 100
```

<span data-ttu-id="e42bd-117">Elenca i primi utenti di annunci di 100 in un tenant.</span><span class="sxs-lookup"><span data-stu-id="e42bd-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="e42bd-118">Esempio 3-ottenere l'utente degli annunci per nome dell'entità utente</span><span class="sxs-lookup"><span data-stu-id="e42bd-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzureRmADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="e42bd-119">Ottiene l'utente dell'annuncio con il nome dell'entità utente " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="e42bd-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="e42bd-120">Esempio 4-elenco per stringa di ricerca</span><span class="sxs-lookup"><span data-stu-id="e42bd-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="e42bd-121">Elenca tutti gli utenti di Active Directory il cui nome visualizzato inizia con "Joe".</span><span class="sxs-lookup"><span data-stu-id="e42bd-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="e42bd-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e42bd-122">PARAMETERS</span></span>

### <span data-ttu-id="e42bd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e42bd-123">-DefaultProfile</span></span>
<span data-ttu-id="e42bd-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e42bd-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e42bd-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e42bd-125">-DisplayName</span></span>
<span data-ttu-id="e42bd-126">Nome visualizzato dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e42bd-126">The display name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42bd-127">-Primo</span><span class="sxs-lookup"><span data-stu-id="e42bd-127">-First</span></span>
<span data-ttu-id="e42bd-128">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="e42bd-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="e42bd-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="e42bd-129">-IncludeTotalCount</span></span>
<span data-ttu-id="e42bd-130">Segnala il numero di oggetti nel set di dati.</span><span class="sxs-lookup"><span data-stu-id="e42bd-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="e42bd-131">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="e42bd-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="e42bd-132">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="e42bd-132">-Mail</span></span>
<span data-ttu-id="e42bd-133">Messaggio di posta elettronica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e42bd-133">The user mail.</span></span>

```yaml
Type: System.String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e42bd-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e42bd-134">-ObjectId</span></span>
<span data-ttu-id="e42bd-135">ID oggetto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e42bd-135">Object id of the user.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e42bd-136">-Skip</span><span class="sxs-lookup"><span data-stu-id="e42bd-136">-Skip</span></span>
<span data-ttu-id="e42bd-137">Ignora i primi oggetti N e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="e42bd-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="e42bd-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="e42bd-138">-StartsWith</span></span>
<span data-ttu-id="e42bd-139">Usato per trovare gli utenti che iniziano con la stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="e42bd-139">Used to find users that begin with the provided string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e42bd-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="e42bd-140">-UserPrincipalName</span></span>
<span data-ttu-id="e42bd-141">UPN dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e42bd-141">UPN of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e42bd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e42bd-142">CommonParameters</span></span>
<span data-ttu-id="e42bd-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e42bd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e42bd-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e42bd-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e42bd-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e42bd-145">INPUTS</span></span>

### <span data-ttu-id="e42bd-146">System. String</span><span class="sxs-lookup"><span data-stu-id="e42bd-146">System.String</span></span>

### <span data-ttu-id="e42bd-147">System. Guid</span><span class="sxs-lookup"><span data-stu-id="e42bd-147">System.Guid</span></span>

## <span data-ttu-id="e42bd-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e42bd-148">OUTPUTS</span></span>

### <span data-ttu-id="e42bd-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="e42bd-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="e42bd-150">Note</span><span class="sxs-lookup"><span data-stu-id="e42bd-150">NOTES</span></span>

## <span data-ttu-id="e42bd-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e42bd-151">RELATED LINKS</span></span>

[<span data-ttu-id="e42bd-152">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="e42bd-152">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)



[<span data-ttu-id="e42bd-153">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="e42bd-153">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

