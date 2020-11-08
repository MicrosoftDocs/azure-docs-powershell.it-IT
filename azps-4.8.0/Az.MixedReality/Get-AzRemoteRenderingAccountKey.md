---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: e9397a2a62ebaa4d26e0d36aaad3fbe03bad137e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033408"
---
# <span data-ttu-id="14a30-101">Get-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="14a30-101">Get-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="14a30-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="14a30-102">SYNOPSIS</span></span>
<span data-ttu-id="14a30-103">Ottenere le chiavi dell'account di rendering remoto</span><span class="sxs-lookup"><span data-stu-id="14a30-103">Get keys of Remote Rendering Account</span></span>

## <span data-ttu-id="14a30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14a30-104">SYNTAX</span></span>

### <span data-ttu-id="14a30-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="14a30-105">DefaultParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14a30-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14a30-106">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14a30-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="14a30-107">PipelineParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14a30-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14a30-108">DESCRIPTION</span></span>
<span data-ttu-id="14a30-109">Ottenere le chiavi dello sviluppatore dell'account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="14a30-109">Get developer keys of Remote Rendering Account.</span></span>

## <span data-ttu-id="14a30-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14a30-110">EXAMPLES</span></span>

### <span data-ttu-id="14a30-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="14a30-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="14a30-112">Ottenere le chiavi dello sviluppatore dell'account di rendering remoto "esempio" dall'abbonamento corrente e dal gruppo di risorse "RG1".</span><span class="sxs-lookup"><span data-stu-id="14a30-112">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="14a30-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="14a30-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | Get-AzRemoteRenderingAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="14a30-114">Ottenere le chiavi dello sviluppatore dell'account di rendering remoto "esempio" dall'abbonamento corrente e dal gruppo di risorse "RG1" con piping.</span><span class="sxs-lookup"><span data-stu-id="14a30-114">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="14a30-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14a30-115">PARAMETERS</span></span>

### <span data-ttu-id="14a30-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14a30-116">-DefaultProfile</span></span>
<span data-ttu-id="14a30-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14a30-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14a30-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14a30-118">-InputObject</span></span>
<span data-ttu-id="14a30-119">Oggetto Domain personalizzato.</span><span class="sxs-lookup"><span data-stu-id="14a30-119">The custom domain object.</span></span>

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

### <span data-ttu-id="14a30-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="14a30-120">-Name</span></span>
<span data-ttu-id="14a30-121">Nome account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="14a30-121">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="14a30-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14a30-122">-ResourceGroupName</span></span>
<span data-ttu-id="14a30-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="14a30-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="14a30-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14a30-124">-ResourceId</span></span>
<span data-ttu-id="14a30-125">ID risorsa dell'account di rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="14a30-125">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="14a30-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14a30-126">CommonParameters</span></span>
<span data-ttu-id="14a30-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14a30-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="14a30-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14a30-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14a30-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="14a30-129">INPUTS</span></span>

### <span data-ttu-id="14a30-130">System. String</span><span class="sxs-lookup"><span data-stu-id="14a30-130">System.String</span></span>

### <span data-ttu-id="14a30-131">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="14a30-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="14a30-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14a30-132">OUTPUTS</span></span>

### <span data-ttu-id="14a30-133">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="14a30-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="14a30-134">Note</span><span class="sxs-lookup"><span data-stu-id="14a30-134">NOTES</span></span>

## <span data-ttu-id="14a30-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14a30-135">RELATED LINKS</span></span>
