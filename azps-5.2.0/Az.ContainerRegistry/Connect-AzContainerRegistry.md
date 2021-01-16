---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: 806fb4892e0fa68b8e49fe29ec0897abf9be2dc8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344680"
---
# <span data-ttu-id="2485a-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2485a-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="2485a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2485a-102">SYNOPSIS</span></span>
<span data-ttu-id="2485a-103">Accedere a un registro di sistema di Azure container.</span><span class="sxs-lookup"><span data-stu-id="2485a-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="2485a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2485a-104">SYNTAX</span></span>

### <span data-ttu-id="2485a-105">WithoutNameAndPasswordParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2485a-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2485a-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="2485a-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2485a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2485a-107">DESCRIPTION</span></span>
<span data-ttu-id="2485a-108">Accedere a un registro di sistema di Azure container.</span><span class="sxs-lookup"><span data-stu-id="2485a-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="2485a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2485a-109">EXAMPLES</span></span>

### <span data-ttu-id="2485a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2485a-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="2485a-111">Accedere a ACR senza credenziali quando si accede già all'account Azure.</span><span class="sxs-lookup"><span data-stu-id="2485a-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="2485a-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2485a-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="2485a-113">Accedere a ACR con il nome utente e la password di amministratore quando l'utente ha abilitato l'amministratore.</span><span class="sxs-lookup"><span data-stu-id="2485a-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="2485a-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="2485a-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="2485a-115">Accedere a ACR con l'ID applicazione e la password di Service Principal.</span><span class="sxs-lookup"><span data-stu-id="2485a-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="2485a-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2485a-116">PARAMETERS</span></span>

### <span data-ttu-id="2485a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2485a-117">-DefaultProfile</span></span>
<span data-ttu-id="2485a-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2485a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2485a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2485a-119">-Name</span></span>
<span data-ttu-id="2485a-120">Nome del registro di sistema di Azure container.</span><span class="sxs-lookup"><span data-stu-id="2485a-120">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2485a-121">-Password</span><span class="sxs-lookup"><span data-stu-id="2485a-121">-Password</span></span>
<span data-ttu-id="2485a-122">Password per il registro dei contenitori di Azure.</span><span class="sxs-lookup"><span data-stu-id="2485a-122">Password For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2485a-123">-UserName</span><span class="sxs-lookup"><span data-stu-id="2485a-123">-UserName</span></span>
<span data-ttu-id="2485a-124">Nome utente per il registro dei contenitori di Azure.</span><span class="sxs-lookup"><span data-stu-id="2485a-124">User Name For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2485a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2485a-125">CommonParameters</span></span>
<span data-ttu-id="2485a-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2485a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2485a-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2485a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2485a-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2485a-128">INPUTS</span></span>

### <span data-ttu-id="2485a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2485a-129">System.String</span></span>

## <span data-ttu-id="2485a-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2485a-130">OUTPUTS</span></span>

### <span data-ttu-id="2485a-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2485a-131">System.Boolean</span></span>

## <span data-ttu-id="2485a-132">Note</span><span class="sxs-lookup"><span data-stu-id="2485a-132">NOTES</span></span>

## <span data-ttu-id="2485a-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2485a-133">RELATED LINKS</span></span>
