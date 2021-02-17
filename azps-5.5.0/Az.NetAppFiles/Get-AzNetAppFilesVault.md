---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
ms.openlocfilehash: 9779db097028710aa8aeddc7a5a1c5bdea85a30a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207075"
---
# <span data-ttu-id="ad13c-101">Get-AzNetAppFilesVault</span><span class="sxs-lookup"><span data-stu-id="ad13c-101">Get-AzNetAppFilesVault</span></span>

## <span data-ttu-id="ad13c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad13c-102">SYNOPSIS</span></span>
<span data-ttu-id="ad13c-103">Recupera l'elenco dei vault di backup dei file ANF di Azure NetApp.</span><span class="sxs-lookup"><span data-stu-id="ad13c-103">Gets list of Azure NetApp Files (ANF) Accounts backup vaults.</span></span>

## <span data-ttu-id="ad13c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad13c-104">SYNTAX</span></span>

### <span data-ttu-id="ad13c-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ad13c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVault -ResourceGroupName <String> [-AccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad13c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad13c-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVault -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad13c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad13c-107">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVault -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad13c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ad13c-108">DESCRIPTION</span></span>
<span data-ttu-id="ad13c-109">Il **cmdlet Get-AzNetAppFilesVault** ottiene l'elenco dei vault di backup degli account ANF.</span><span class="sxs-lookup"><span data-stu-id="ad13c-109">The **Get-AzNetAppFilesVault** cmdlet gets list of an ANF accounts backup vaults.</span></span>

## <span data-ttu-id="ad13c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad13c-110">EXAMPLES</span></span>

### <span data-ttu-id="ad13c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ad13c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesVault -ResourceGroupName "MyRG" -AccountName "MyAnfAccount"
```

<span data-ttu-id="ad13c-112">Questo comando ottiene un elenco dei vault di backup per l'account Azure NetappFiles (ANF) "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="ad13c-112">This command gets a list of the backup vaults for Azure NetappFiles (ANF) account "MyAnfAccount".</span></span>

## <span data-ttu-id="ad13c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad13c-113">PARAMETERS</span></span>

### <span data-ttu-id="ad13c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ad13c-114">-AccountName</span></span>
<span data-ttu-id="ad13c-115">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="ad13c-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad13c-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="ad13c-116">-AccountObject</span></span>
<span data-ttu-id="ad13c-117">Account per il nuovo oggetto di backup</span><span class="sxs-lookup"><span data-stu-id="ad13c-117">The account for the new backup object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad13c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad13c-118">-DefaultProfile</span></span>
<span data-ttu-id="ad13c-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad13c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad13c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad13c-120">-ResourceGroupName</span></span>
<span data-ttu-id="ad13c-121">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="ad13c-121">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad13c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad13c-122">-ResourceId</span></span>
<span data-ttu-id="ad13c-123">ID risorsa del pool ANF</span><span class="sxs-lookup"><span data-stu-id="ad13c-123">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad13c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad13c-124">CommonParameters</span></span>
<span data-ttu-id="ad13c-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad13c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad13c-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ad13c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad13c-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="ad13c-127">INPUTS</span></span>

### <span data-ttu-id="ad13c-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="ad13c-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="ad13c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ad13c-129">System.String</span></span>

## <span data-ttu-id="ad13c-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad13c-130">OUTPUTS</span></span>

### <span data-ttu-id="ad13c-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="ad13c-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="ad13c-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="ad13c-132">NOTES</span></span>

## <span data-ttu-id="ad13c-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad13c-133">RELATED LINKS</span></span>
