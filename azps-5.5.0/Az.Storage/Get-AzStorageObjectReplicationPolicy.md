---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 6785eac6df5568f4b26e6de61ac0f4bfd8061259
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201319"
---
# <span data-ttu-id="b1885-101">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="b1885-101">Get-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="b1885-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1885-102">SYNOPSIS</span></span>
<span data-ttu-id="b1885-103">Ottiene o elenca i criteri di replica degli oggetti di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b1885-103">Gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="b1885-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1885-104">SYNTAX</span></span>

### <span data-ttu-id="b1885-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b1885-105">AccountName (Default)</span></span>
```
Get-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1885-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b1885-106">AccountObject</span></span>
```
Get-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1885-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b1885-107">DESCRIPTION</span></span>
<span data-ttu-id="b1885-108">Il cmdlet **Get-AzStorageObjectReplicationPolicy** ottiene o elenca i criteri di replica degli oggetti di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b1885-108">The **Get-AzStorageObjectReplicationPolicy** cmdlet gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="b1885-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1885-109">EXAMPLES</span></span>

### <span data-ttu-id="b1885-110">Esempio 1: Ottenere un criterio di replica degli oggetti con un ID criterio specifico e visualizzarne le regole.</span><span class="sxs-lookup"><span data-stu-id="b1885-110">Example 1: Get an object replication policy with specific policy Id and show its rules.</span></span>
```
PS C:\> $policy = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" -PolicyId 56bfa11c-81ef-4f8d-b307-5e5386e16fba

PS C:\> $policy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]

PS C:\> $policy.Rules

RuleId                               SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------                               --------------- -------------------- ------------------- -----------------------
d3d39a01-8d92-40e5-849f-e56209ae5cf5 src1            dest1                {}                                         
2407de9a-3301-4656-858f-359d185565e0 src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="b1885-111">Questo comando recupera un criterio di replica degli oggetti con un ID criterio specifico e ne mostra le regole.</span><span class="sxs-lookup"><span data-stu-id="b1885-111">This command gets an object replication policy with specific policy Id and show its rules.</span></span>

### <span data-ttu-id="b1885-112">Esempio 2:Elencare i criteri di replica degli oggetti da un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b1885-112">Example 2:List object replication policy from a Storage account</span></span>
```
PS C:\> $policies = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" 

PS C:\> $policies

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysrcaccount1   mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
myresourcegroup   mydestaccount      68434c7a-20d0-4282-b75c-43b5a243435e             mysrcaccount2   mydestaccount      [d3d39a01-8d92-40e5-849f-e56209ae5cf5,...]
```

<span data-ttu-id="b1885-113">Questo comando elenca i criteri di replica degli oggetti da un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b1885-113">This command lists object replication policy from a Storage account.</span></span>

## <span data-ttu-id="b1885-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1885-114">PARAMETERS</span></span>

### <span data-ttu-id="b1885-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1885-115">-DefaultProfile</span></span>
<span data-ttu-id="b1885-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1885-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1885-117">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="b1885-117">-PolicyId</span></span>
<span data-ttu-id="b1885-118">ID dei criteri di replica degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="b1885-118">Object Replication Policy Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1885-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1885-119">-ResourceGroupName</span></span>
<span data-ttu-id="b1885-120">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b1885-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1885-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b1885-121">-StorageAccount</span></span>
<span data-ttu-id="b1885-122">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b1885-122">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1885-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b1885-123">-StorageAccountName</span></span>
<span data-ttu-id="b1885-124">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b1885-124">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1885-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1885-125">CommonParameters</span></span>
<span data-ttu-id="b1885-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1885-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1885-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1885-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1885-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="b1885-128">INPUTS</span></span>

### <span data-ttu-id="b1885-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b1885-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="b1885-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1885-130">OUTPUTS</span></span>

### <span data-ttu-id="b1885-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="b1885-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="b1885-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="b1885-132">NOTES</span></span>

## <span data-ttu-id="b1885-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1885-133">RELATED LINKS</span></span>
