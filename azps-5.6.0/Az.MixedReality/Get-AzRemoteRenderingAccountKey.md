---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/get-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: 03cb387b77dc2f003277b9f04a482f88a8da86fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958670"
---
# <span data-ttu-id="7ae55-101">Get-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="7ae55-101">Get-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="7ae55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ae55-102">SYNOPSIS</span></span>
<span data-ttu-id="7ae55-103">Ottenere le chiavi dell'account di rendering remoto</span><span class="sxs-lookup"><span data-stu-id="7ae55-103">Get keys of Remote Rendering Account</span></span>

## <span data-ttu-id="7ae55-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ae55-104">SYNTAX</span></span>

### <span data-ttu-id="7ae55-105">DefaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="7ae55-105">DefaultParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ae55-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ae55-106">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ae55-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ae55-107">PipelineParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ae55-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7ae55-108">DESCRIPTION</span></span>
<span data-ttu-id="7ae55-109">Ottieni le chiavi per sviluppatori di Remote Rendering Account.</span><span class="sxs-lookup"><span data-stu-id="7ae55-109">Get developer keys of Remote Rendering Account.</span></span>

## <span data-ttu-id="7ae55-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ae55-110">EXAMPLES</span></span>

### <span data-ttu-id="7ae55-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7ae55-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="7ae55-112">Ottenere le chiavi per sviluppatori di Remote Rendering Account "example" dalla sottoscrizione corrente e dal gruppo di risorse "rg1".</span><span class="sxs-lookup"><span data-stu-id="7ae55-112">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="7ae55-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7ae55-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | Get-AzRemoteRenderingAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="7ae55-114">Ottenere le chiavi per sviluppatori di Remote Rendering Account "example" dalla sottoscrizione corrente e dal gruppo di risorse "rg1" con piping.</span><span class="sxs-lookup"><span data-stu-id="7ae55-114">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="7ae55-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ae55-115">PARAMETERS</span></span>

### <span data-ttu-id="7ae55-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ae55-116">-DefaultProfile</span></span>
<span data-ttu-id="7ae55-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7ae55-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae55-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ae55-118">-InputObject</span></span>
<span data-ttu-id="7ae55-119">Oggetto dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="7ae55-119">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae55-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7ae55-120">-Name</span></span>
<span data-ttu-id="7ae55-121">Nome dell'account per il rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="7ae55-121">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae55-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ae55-122">-ResourceGroupName</span></span>
<span data-ttu-id="7ae55-123">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7ae55-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae55-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ae55-124">-ResourceId</span></span>
<span data-ttu-id="7ae55-125">ID risorsa dell'account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="7ae55-125">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae55-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ae55-126">CommonParameters</span></span>
<span data-ttu-id="7ae55-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ae55-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7ae55-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ae55-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ae55-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="7ae55-129">INPUTS</span></span>

### <span data-ttu-id="7ae55-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7ae55-130">System.String</span></span>

### <span data-ttu-id="7ae55-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="7ae55-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="7ae55-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ae55-132">OUTPUTS</span></span>

### <span data-ttu-id="7ae55-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7ae55-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="7ae55-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="7ae55-134">NOTES</span></span>

## <span data-ttu-id="7ae55-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ae55-135">RELATED LINKS</span></span>
